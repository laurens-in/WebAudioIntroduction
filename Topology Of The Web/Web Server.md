A web server is a specific kind of server that listens to HTTP requests. There are two kinds of web servers: static and dynamic.

Static web servers can only send **static** files such as [[HTML]], [[CSS]], [[JavaScript]] or [other supported file types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types). This means that the server can only send the files as they are and does not manipulate them. In this class we will only use static web servers. Static web pages are also called _client-side rendered_.

Dynamic web servers can manipulate the content of files before they are being sent to a client. They include a runtime for server-side scripting languages such as [[Node.js]], PHP, Python and many more. They are not only used to serve web pages but also data APIs. Dynamic web pages are also called _server-side rendered_.

Normally, servers expect a file called `index.html` to be at the root of our site. This file will automatically be served if someone accesses our server without asking for a specific file.
