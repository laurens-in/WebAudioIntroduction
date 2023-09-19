You will see this term during development. All this means is that we are running a server - or _host_ - on our local machine. Localhost uses the IP address `127.0.0.1.` and can be accessed by typing it into our browser address bar. 

Normally we also need to specify the port on which our host is running. For normal servers, these ports are standardized and thus don't need to be specified, the browser will know which ports to use. Localhost however can use any port it likes, but your development server will tell you on which port it is running.

In most browsers, we can use the address `http://localhost:<port>` and it the browser will know that we want to access the host with IP `127.0.0.1.`

Essentially what we are doing when we connect to the localhost is connecting to our own machine (loopback). This means that we are simultaneously take the role of server and client
