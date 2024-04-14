What happens when...
====================

This repository is an attempt to answer the age-old interview question "What
happens when you type google.com into your browser's address box and press
enter?"

Except instead of the usual story, we're going to try to answer this question
in as much detail as possible. No skipping out on anything.

This is a collaborative process, so dig in and try to help out! There are tons
of details missing, just waiting for you to add them! So send us a pull
request, please!

This is all licensed under the terms of the `Creative Commons Zero`_ license.

Read this in `简体中文`_ (simplified Chinese), `日本語`_ (Japanese), `한국어`_
(Korean) and `Spanish`_. NOTE: these have not been reviewed by the alex/what-happens-when
maintainers.

**What happens when you type https://www.google.com in your browser and press Enter?**

When you type https://www.google.com into your web browser and hit Enter, a seemingly simple action triggers a complex web of interactions between your computer and the remote servers hosting the Google search engine. This complex process is a dance of internet protocols, security checks, and network communications that seamlessly bring the world's information to your fingertips. Let's break down this fascinating journey step by step.
In this blog, we will cover different concepts, such as **_DNS Request_**, **_TCP/IP_**, **_Firewall_**, **_HTTPS/SSL_**, **_Load-balancer_**, **_Web server_**, **_Application server_**, **_Database_**

**1. DNS Request**

![DNS](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nph8k3u3e0w99t502uje.png)

The journey begins with a DNS (Domain Name System) request. Think of DNS as the Internet's phonebook. When you type https://www.google.com, your browser needs to know where Google's website is. It needs www.google.com to be translated into an IP (Internet Protocol) address that computers understand. Your browser asks a DNS (Domain Name Service) resolver for the IP address associated with that domain name. The resolver, often provided by your ISP (Internet Service Provider), checks its cache, and if it doesn't find the address, it queries other DNS servers worldwide. Once it retrieves the IP address, it sends it back to your browser.

**2. TCP/IP**

![TCP/IP](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oxwyi13mb4nqk62kj5wv.jpeg)

With the IP address in hand, your browser can establish a connection to Google's server. This is done using TCP/IP (Transmission Control Protocol/Internet Protocol), which governs how data is sent and received over the Internet. TCP breaks down your request into smaller packets, labels them to ensure they're reassembled in the correct order, and sends them across the Internet. IP is responsible for routing these packets from your device to the destination server.

**3. Firewall**

![Firewall](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9i7uda7sz90yx9t1cviq.png)

As these data packets travel, they encounter firewalls. A firewall is a security system that monitors incoming and outgoing network traffic based on predetermined security rules. Your local machine and Google's servers have firewalls to prevent unauthorized access. These firewalls inspect the packets to ensure they're not malicious before passing them through.

**4. HTTPS/SSL**

![HTTPS](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f2tnkz7q6rds41m4b3fd.png)

The https in The URL indicates that the connection between your browser and Google's server will be secure, using HTTPS (Hypertext Transfer Protocol Secure) with SSL (Secure Sockets Layer) encryption. SSL encrypts the data exchanged to prevent eavesdropping or tampering by third parties. When your browser connects to Google's server, it requests a copy of the server's SSL certificate. If the certificate is valid, a secure connection is established.

**5. Load-balancer**
![Load balancer](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6yhbafyql7bcxiuz8dyl.png)

Google receives millions of requests per second, which is far too much for a single server to handle. Enter the load balancer, which distributes incoming network traffic across multiple servers. This ensures no single server is overwhelmed and helps to optimize resource use, maximize throughput, minimize response time, and avoid overload of any single resource.

**6. Web Server**
![Web server](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kqyv0qrjeknkb9vjd6cp.png)

Once your request reaches Google's infrastructure, it's handled by a web server. This server's job is to serve web content. When it receives your request for https://www.google.com, it fetches the necessary HTML, CSS, and JavaScript files that make up the Google search page.

**7. Application Server**
![Application Server](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/p7x41d3v15stx3pgrll1.jpeg)

While the web server serves static content, an application server handles the application's business logic. For Google, this includes executing search algorithms, personalizing content based on your profile, and ensuring that the search results are retrieved efficiently.

**8. Database**
![Database](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/afp5iqg59m2pfsifp9cn.png)

Finally, the application server interacts with databases that store all the data Google needs to provide you with search results. This could be indexing information, user data, or cached content. When you perform a search, the application server queries these databases to retrieve and display the most relevant search results.

In summary, when you type https://www.google.com and press Enter, it is like starting a rapid-fire sequence of events in the digital world. Each step, from DNS requests to database queries, involves sophisticated technology and coordination.
This entire process happens in the blink of an eye, illustrating the incredible power and complexity of the Internet infrastructure we often take for granted.
Understanding this process satiates our curiosity and helps us appreciate the marvel of modern internet communications, a crucial skill set for any aspiring tech professional.

You can also find related blogs on [my LinkedIn](https://www.linkedin.com/pulse/what-happens-when-you-type-httpswwwgooglecom-your-browser-nzamuwe-knbvf/) or [Dev.to](https://dev.to/princenzmw/what-happens-when-you-type-httpswwwgooglecom-in-your-browser-and-press-enter-556p)

.. _`Creative Commons Zero`: https://creativecommons.org/publicdomain/zero/1.0/
.. _`"CSS lexical and syntax grammar"`: http://www.w3.org/TR/CSS2/grammar.html
.. _`Punycode`: https://en.wikipedia.org/wiki/Punycode
.. _`Ethernet`: http://en.wikipedia.org/wiki/IEEE_802.3
.. _`WiFi`: https://en.wikipedia.org/wiki/IEEE_802.11
.. _`Cellular data network`: https://en.wikipedia.org/wiki/Cellular_data_communication_protocol
.. _`analog-to-digital converter`: https://en.wikipedia.org/wiki/Analog-to-digital_converter
.. _`network node`: https://en.wikipedia.org/wiki/Computer_network#Network_nodes
.. _`TCP congestion control`: https://en.wikipedia.org/wiki/TCP_congestion_control
.. _`cubic`: https://en.wikipedia.org/wiki/CUBIC_TCP
.. _`New Reno`: https://en.wikipedia.org/wiki/TCP_congestion_control#TCP_New_Reno
.. _`congestion window`: https://en.wikipedia.org/wiki/TCP_congestion_control#Congestion_window
.. _`maximum segment size`: https://en.wikipedia.org/wiki/Maximum_segment_size
.. _`varies by OS` : https://en.wikipedia.org/wiki/Hosts_%28file%29#Location_in_the_file_system
.. _`简体中文`: https://github.com/skyline75489/what-happens-when-zh_CN
.. _`한국어`: https://github.com/SantonyChoi/what-happens-when-KR
.. _`日本語`: https://github.com/tettttsuo/what-happens-when-JA
.. _`downgrade attack`: http://en.wikipedia.org/wiki/SSL_stripping
.. _`OSI Model`: https://en.wikipedia.org/wiki/OSI_model
.. _`Spanish`: https://github.com/gonzaleztroyano/what-happens-when-ES
