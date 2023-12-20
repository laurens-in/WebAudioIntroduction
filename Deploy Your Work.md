If you want to deploy your page to the internet - make it accessible for everyone - then there's a lot of possibilities.

I will show you one possibility here, but if it doesn't suite your needs then don't worry, there are other ways.

Since we are already using git and Github, we will use Github Pages to deploy our static page. As a prerequesite you need a folder with a vite project.

You will set up the deployment as a part of Github Actions. Github Actions are automated workflows that can be triggered by certain actions you take. Specifically we are going to trigger the deployment every time your main branch is updated. 

Then you can follow this great [write-up](https://github.com/sitek94/vite-deploy-demo/blob/main/README.md) created by [Maciek Sitkowski](https://github.com/sitek94). It covers all steps you need to take in great detail.

There's an additional [write-up](https://github.com/sitek94/vite-deploy-demo-custom-domain) of his, where he explains how to add a custom domain. However there's a crucial step missing. You need to put a file called CNAME in the root of your repository. In this file you put the domain where your site should be hosted:

```
# CNAME
example.com
```

Then in your Github Actions workflow file, you include the following change inside the build job:

```yaml
jobs:
  build:
    name: Build
    runs-on: ubuntu-latest
    
  steps:
    - name: Checkout repo
      uses: actions/checkout@v3
      
    - name: Setup Node
      uses: actions/setup-node@v3
    
    - name: Install dependencies
      run: npm ci
    
    - name: Build project
      run: npm run build

    # Add the following step!
    - name: Add CNAME
      run: cp CNAME ./dist/CNAME
    
    - name: Upload production-ready build files
      uses: actions/upload-artifact@v3
      with:
        name: production-files
        path: ./dist
```

Now your site should deploy without a problem!
