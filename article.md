
Have you ever wondered what happens when you type a URL into your browser’s address bar, like https://www.google.com? I asked to a few friends about their thoughts.

Mr. Ayodeji Aladejana had an interesting take that,Google, the company, will somehow print out the information you’re searching for. On the other hand, Mr. Andrew Daniel suggested that entering the URL would simply take you to Google’s servers. Both answers are quite True.

In this article I intend to explain in the simplest terms what happens when you enter the url https://www.google.com into your browser. Along the way we would touch a little networking terms like DNS Request, tcp/ip, firewall, https/ssl, load balancers, webservers, application servers and databases.

Now, let’s ‘DELVE’ into what truly Happens when you enter a URL into your browser.

Before we proceed, its important we know that, communication between computers happens through IP addresses. Every device connected to the internet has its unique identifier, known as an IP address. So, when you enter a URL into your browser, your computer sends a request using the TCP(Transmission Control Protocol) to reach out to Google’s servers where the requested information resides.

Before proceeding further, let’s take a moment to consider the importance of security when making requests over the internet. This is where HTTPS/SSL comes into play. HTTPS/SSL protocols ensure the security and authentication of your requests, safeguarding your data as it travels across the web.

Now, let’s talk about DNS. When you make a request over the internet, it’s crucial to understand that your computer communicates using private IP addresses, which aren’t directly accessible from the broader internet. Here’s where a DNS (Domain Name System) server steps in. It translates your private IP address into a publicly accessible IP address that can be used to fulfill your request securely.

Once the request reaches Google’s servers, it encounters a load balancer. Load balancers play a very important role in distributing incoming traffic across multiple servers to ensure peak performance and prevent one server from becoming overloaded and overworked. This ensures that your request is efficiently handled, regardless of the current load on Google’s infrastructure.

After passing through the load balancer, your request reaches a web server. Web servers are responsible for receiving and responding to HTTP requests, serving web pages, and handling other web-related tasks. Examples of webservers include, Nginx and Apache Webservers. In this case, the web server at Google processes your request and retrieves the necessary data.

Next up is the application server. Application servers execute the logic and code required to generate dynamic content or perform specific functions requested by the user. They work closely with the web server to process and fulfill your request effectively.

Finally, the data you requested may be stored in a database. Databases are used to organize, store, and retrieve data in a structured manner. In the context of Google’s search engine, the database likely contains vast amounts of indexed web pages and other relevant information.





