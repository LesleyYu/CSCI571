## HTML5

#### new features in HTML5:

1. Canvas
   1. Interactive Gradient 

2. Web Forms improvements
3. Offline web applications
4. Drag and drop
5. editable content
6. Storage 
7. ~~Network-based storage~~
8. ~~Local SQL database~~

#### Elements removed from HTML5

• **basefont, big, center, font, s, strike, tt, u**

​	Reason:  their effect is purely presentational and therefore better handled by CSS

• **frame , frameset, noframes**

​	Reason:  their usage affected usability and accessibility for the end user in a negative way

• **acronym** is not included because it has created lots of confusion. Authors are to use *abbr* for abbreviations.

• **applet** has been obsoleted in favor of *object*.

• **isindex** usage can be replaced by usage of form controls.

• **dir** has been obsoleted in favor of *ul*.

#### Vector graphics - SVG

* The <svg> element is “a container for SVG graphics.”
* SVG has methods for drawing paths, boxes, circles, text and graphviz images.
* SVG supports animations, filters, effects, etc…
* SVG graphics is supported by all major browsers.
* SVG is a language for describing 2D graphics in XML.
* Since SVG is XML based, every element is available in the SVG DOM.

#### Canvas vs. SVG

![image-20250428213218962](/Users/lesley/Documents/USC/CSCI571/pastPapers/pics/canvasVSsvg.png)

The 2 most popular HTML5 video codecs: **H.264**, **VP9**



## RWD

* Switching between display `x.style.display = "block";` and `x.style.display = "none";` may be used in RWD.

* The major difference between different versions of Bootstrap is the number of grid tiers.

* RWD) is a web design approach that tries to achieve an ideal viewing experience, which means:

  * easy reading and navigation with a minimum of or no resizing, panning, and scrolling
  * across a wide range of devices (from mobile phones to desktop monitors)

* A site designed with RWD adapts the layout to the viewing environment by using

  1. **fluid**, proportion-based **grids**,

  2. **flexible images**, and

  3. CSS3 **media queries**

* **Q:**

  ❌ Uses CSS3 media queries, adaptive grids and flexible images

  ✅ No panning if possible, unless required by the application

  ❌ Easy reading with a minimum of scrolling		？？？

  ✅ Adapts to viewing environment
  
* Reasons why hosting a `.mobi` website is not recommended.

  ❌ It hinders search engines  (--> This is the reason for hosting a `mobile.xxx.com` website)

  ✅ Requires duplication of content

  ✅ Results in content synchronization issues

  ❌ Will work on multiple device sizes
  
  ✅ Nobody is using .mobi TLDs
  
  ❌ Redirect take time

* Reasons for not using `mobile.mycompany.com` websites
  1. Redirects can **hinder/annoy search engines**
  2. **Redirects** take lots of time
  3. If you offer a mobile.website for iPhone, what about for **iPad, Android**, etc.
  4. **Sharing a mobile.website will not work for all users** people on laptops  will end up with a site designed for a small screen



### fluid grids

* In “*fluid grids*” we define **relative-based dimensions**.

​	– Since fluid grids flow naturally within the dimensions of its parent container, limited adjustments will be needed for various screen sizes and devices.

* In fluid grids we

1. **Define** a maximum layout **size** for the design.

2. The grid is divided into a specific number of columns to keep the layout clean and easy to handle.

3. Then we design each element with proportional widths and heights instead of pixel-based dimensions.

##### Q

Select RWD usability guidelines on mobile devices.

A. reduce amount of content

B. maximize text entry

C. use single or two columns

D. change navigation

Answer: A&D. 

A: yes. trim non-essential text.

B: minimize them

C: not a guideline. 

D: Wide desktop nav bars rarely fit on mobile. 





## REST Web Services

#### Fundamental aspects of REST Design Pattern

There are three fundamental aspects of the REST Design Pattern

* 1. **client**, 2. **servers**, 3. **<u>resources</u>**

* Resources are typically represented as **documents**
* Systems that follow Fielding's REST principles are often referred to as **RESTful**;

![image-20250428234141154](/Users/lesley/Documents/USC/CSCI571/pastPapers/pics/RESTfundamentals.png)

#### More Complex REST Requests

* REST can easily handle more complex requests, including multiple parameters.
* All types of HTTP requests: **GET, POST, PUT, PATCH, DELETE, HEAD, OPTIONS**
* Rarely used: **LINK, UNLINK, PURGE**

* If you need to pass long parameters, or binary ones, you'd normally use HTTP POST requests and include the parameters in the POST body.

* As a rule,

  1. **GET** requests should be for read-only queries; they should not change the state of the server and its data, List all items, for example.

  2. For creation, use **POST** requests. POST can also be used for read-only queries, as noted above, when complex params are required.’

  3. **PUT**, **DELETE** are also used for updating and deleting items, respectively.

#### REST Best Practices

1. Provide a **URI for each resource** that you want exposed.

2. Prefer URIs that are logical over URIs that are physical. For example, prefer

   http://www.boeing.com/airplanes/747

   Over:

   http://www.boeing.com/airplanes/747.html

   Logical URIs allow **the resource implementation to change** without impacting client applications

3. As a corollary to (2) **use nouns in the logical URI, not verbs**. Resources are "things“ not "actions"

4. Make all HTTP GETs **side-effect free**.

5. Use **links** in your responses to requests. Doing so connects your response with other data. It enables client applications to be self-propelled. That is, the response itself contains info about "what's the next step to take".

6. **Minimize the use of query strings**. For example, prefer 

   http://www.parts-depot.com/parts/00345

   Over

   http://www.parts-depot.com/parts?part-id=00345

7. Use the slash "/" to represent a parent-child, whole-part relationship

8. Use a **"gradual unfolding methodology"** for exposing data to clients. That is, a resource representation should provide links to obtain more details.

9. Always implement a service **using HTTP GET** when the purpose of the service is to allow a client to **retrieve a resource representation**, i.e., don’t use HTTP POST



* In REST Web Services, plain text and CSV format may be used in formatting the responses.
* REST services are **NOT** a W3C recommendation
* REST services can use HTTPS === For encryption, REST can be used on top of **HTTPS** (secure sockets).
* **XML-RPC protoco**l and **REST** use HTTP as a **transport**.



## Severless

#### Definition

Serverless architectures refer to applications that significantly depend on <u>third party-services (known as Backend as a Service or “Baas”)</u> or on <u>custom code that’s run in ephemeral containers (Function as a Service or “FaaS”)</u>, the best known vendor host of which currently is **AWS Lambda**. By using these ideas,and by moving much behavior to the front end, such architectures remove the need for the traditional ‘always on’ server system sitting behind an application.

#### Features of Serverless Architectures

* **No compute resource to manage** ‼️
* **Provisioning and scaling** handled by **service** itself
* You write code and the **execution environment** is provided by the **service**
* Core funtionality (e.g. database, authentication and authorization) is provided by **at-scale Web Services**

##### 	Q

​	Select which of the following are true of Serverless Architectures. Select all that apply.

​	A. Execution environment provided by service

​	B. Provide authorization and authentication services

​	C. No compute resource to manage

​	D. Provisioning and scaling handled by the client

​	Answer: ABC



### Function-as-a Service (FaaS) 

The **origins** of FaaS: AWS Lambda, API Gateway

**How** does it work: You write a function and deploy it to the cloud service for execution.

#### FaaS的下一步

* Polyglot language support (each function written in a different language)
* stateful endpoints (web sockets)
  * **stateful** meaning:  the connection between client and server will stay alive until it gets terminated by either party (client or server).
  * AWS Lambda implements WebSockets by integrating the Fanout service
* Remote Debugging
* Enhanced Monitoring 
  * AWS explanation: a tool that captures metrics in real time for the operating system (OS) that your Amazon RDS DB instance runs on.
* Evolution of CI/CD Patterns
  * Continuous Integrating / Continuous Deployment
* IDE's
* [Ten Attributes of Serverless Computing Platforms](https://thenewstack.io/serverless/ten-attributes-serverless-computing-platforms/)
  1. **Polyglot Platform**
  2. Support For Sync and Async Invocation
  3. **API Gateway Integration**
  4. Developer Productivity
  5. Support for DevOps and Tooling
  6. Responsiveness and Performance
  7. **Logging and Monitoring**
  8. REST Endpoints and Automation
  9. Support Long-running Jobs and Batch Processing (i.e. **Job scheduling**)
  10. Extensibility and Integration



##### Q

What are issues that need additional work for FaaS? Select all that apply.

A. Billing 

B. Polyglot language support 

C. Remote debugging 

D. IDE's

Answer: BCD.



### Backend-as-a-Service (BaaS)  (没考到)

* Data Stores
  * NoSQL Databases; BLOB Storage; Cache (CDN)

* Analytics

  * Query; Search; Stream Processing

  * IoT

* AI

  * ML

  * Image Recognition

  * NLP/Understanding

  * Speech to Text/Text to Speech

#### BaaS 的下一步  (没考到)

* Database
  * Graph

* Analytics
  * Query; Search; Stream Processing

* AI

  * Fraud detection 
  * Latent sematic analysis

* Geospatial

  * Satellite imagery

  * Hyper-Locality

* HPC (High Performance Computing)



### Containers 

Key Features: 

 	1. **Lightweight**
 	 	1. All containers running on the same host share a single Linux kernel
 	 	2. Container images don’t require a full OS install like a virtual machine (**VM**) image
 	2.  **Portable**
 	 	1. Execution environment abstracts the underlying host from the container
 	 	2. No dependency on a specific virtual machine technology
 	 	3. Container images can be shared using GitHub-like repositories, such as **DockerHub** (hub.docker.com)

#### Containers 的下一步

* Networking
  * Overlay networks between containers running across separate hosts
* Stateful Containers
  * suppoer for container architectures that read and write persistent data
* Monitoring and Logging
  * Evolution of design patterns for capturing telemetry and log data from running containers
    * **Telemetry** refers to *the collection, transmission, and measurement of data*.

* Debugging
  * Attach to running containers and debug code
* security
  * Better isolation at the kernel level between containers running on the same host
  * Secret/Ket management - Transparently pass sensitive configuration

##### Q: 

Select features of a "container." Select all that apply.

A. portable

B. made mainstream by Docker

C. requires a VM

Answer: AB



### Serverless Architecture - Microservices

![image-20250501012439838](/Users/lesley/Documents/USC/CSCI571/pastPapers/pics/ServerlessArchitecture-Microservices.png)

### AWS Lambda

#### Example Architecture

* Search
* Location-Awareness
* Machine-learning powered recommendations
* **NoSQL**
* Microservices
* API Management
* Static website with CDN
* Not a single server to manage!

#### AWS Lambda

* Compute Service using Amazon's infrastructure
* Code === function
* Supported – Java, Python and Node.js (i.e., JavaScript)
* Can say it to be Docker under the covers
* A system that uses Linux Containers
* **Pay only for the compute time you use**
* **Triggered by events** or called from **HTTP**
* It still **has SERVERS**, but we do not care about them
* **Functions** are unit of deployment and scaling
* No Machines, no Vms or containers visible in Programming Model
* **Never pay for idle**
* Auto-Scaling and Always Available, **adapts to rate of incoming requests**

#### Using AWS Lambda

* **No Servers** to Manage
* Continuous Scaling
* Subsecond metering
* Bring your own code
* **Simple resource model**
* Flexible Authorization and Use
* Stateless but you can connect to others to store state
* Authoring functions
* Makes it easy to

​		– Perform **real time data processing**

​		– Build **scalable backend services**

​		– Glue and choreograph systems

##### Q

To determine whether a piece of serverless code is for **AWS Lambda** or **Google Cloud Function (GCF)**:

##### AWS Lambda Keywords / Patterns

Look for:

- exports.handler = async (event, context) => { ... }
- event, context parameters
- Use of AWS SDK (e.g., require('aws-sdk'))
- IAM role mentions
- Environment variables prefixed by AWS_
- Deployment/config mentions of .zip packaging or CloudFormation

**Example:**

```js
exports.handler = async (event, context) => {
  console.log("Request ID:", context.awsRequestId);
  return { statusCode: 200, body: "Hello from Lambda!" };
};
```

##### Google Cloud Function (GCF) Keywords / Patterns

Look for:

- exports.functionName = (req, res) => { ... } (HTTP function)
- exports.functionName = (event, context) => { ... } (Background/event function)
- Use of req, res (like Express)
- GCP SDK (e.g., @google-cloud/storage)
- Environment variables prefixed by GCP_ or FUNCTION_

Example:

```js
exports.helloWorld = (req, res) => {
  res.send("Hello from Google Cloud Function!");
};
```



## Cookies and Privacy

### Definition

Short pieces of text generated during web activity and stored in the user’s machine by the user’s web browser for future reference.

### Contains:

**Name**, **value**, **path** and **expiration date**

### Cookies can:

✅ Track user **IP address**.

✅ Track user visits.

✅ Store site information.

### Advertising on the Web

An **online advertising network** or **ad network** is a company that connects advertisers to web sites that want to host advertisements.

##### 4 Key Player:

1. **advertisers** that wish to place the ads.
2.  **website owners**: make money by selling ad space on their websites.

3.  **Ad Network**: signs up advertisers and places their ads on the web pages of website owners.
4. **visitors** who view the web pages that contain the ads.



#### Six Ways to Opt Out of cookies

1. Select “do not track” in your browser Settings.

2. **Download** opt-out cookies. 

3. Use the cookie management tools in your web browser.

4. View current cookies and delete what you don't need.

5. Check your account preferences on registration sites.

6. **Use browser Add-ons**. 

##### Q (Opt-out cookies)

Select all ways to "opt out" of cookies. Select all that apply.

A. Use cookie management tool in browser

B. Install browser extensions

C. Select "do not track" in browser

D. Download opt-out cookie

E. Change account Preferences on registration sites

Answer : all



### HttpOnly

✅ A cookie with HttpOnly attribute can only be accessed by the web server.

✅ The HttpOnly attribute tells the browser not to make it discoverable through document.cookie.

❌ A cookie with HttpOnly attribute can only be accessed through a secure connection.

✅ A cookie with HttpOnly attribute cannot be accessed via client-side scripting languages.

✅ A cookie with HttpOnly attribute cannot be stolen easily via cross-site scripting attacks.



## JS Frameworks

### Node.js

Node.js is a JavaScript <u>runtime</u> built on **Chrome's V8 JavaScript engine**.

Node.js uses an <u>event-driven, non-blocking I/O model</u> that makes it <u>lightweight and efficient</u>.

Node.js allows the creation of <u>Web servers</u> and <u>networking tools</u> using JavaScript and a collection of "<u>modules</u>" that handle various core functionality.

Modules handle <u>file system I/O</u>, <u>networking</u> (**DNS, HTTP, TCP, TLS/SSL, or UDP**, does not handle: ~~**IP**~~), <u>binary data</u> (buffers), <u>cryptography</u> functions, <u>data streams</u> and other core functions.

#### React

❌ Is a framework like Angular

✅ Does not implement MVC

### Typescript

* Open-source programming language developed and maintained by Microsoft
* Syntactical superset of JavaScript
* Developed by **Anders Hejlsberg**, C# Architect and creatorof Turbo Pascal
* First made public in October **2012** (version 0.8)
* Built-in support for TypeScript in Visual Studio 2013+
* Latest version is **TypeScript 5.8.3** (4th April, 2025)
* TypeScript program can seamlessly consume JavaScript

* TypeScript compiler written in TypeScript

#### Features:

1. Type annotations and compile-time type checking
2. Type inference
3. Type erasure
4. Interfaces
5. Enumerated type:  `Enum`
6. Mixin
7. Generic
8. Namespace
9. Tuple
10. Await
11. **Classes**
12. **Modules**
13. Arrow syntax for anonymous functions
14. **Optional** and default parameters



## AJAX

✅ AJAX stands for Asynchronous JavaScript and XML.

✅ AJAX allows for just **part of a page** to be **reloaded** with direct access to the server.

✅ AJAX uses JavaScript and HTML DOM to display the data.

✅ AJAX applications can transport data as JSON text

✅ AJAX **uses** a browser built-in **XMLHttpRequest** object to communicate with the server

✅ Updates to a page made via AJAX are displayed dynamically **without refreshing the page**.

✅ AJAX can be performed <u>on submission of a form</u> by adding the onsubmit parameter in the form tag

### AJAX open()

Q: During AJAX open(), what does it mean to pass in <false> to the third parameter and why is it poor practice?

A: False means the request will be executed synchronously. It is bad because a time-consuming synchronous request on the main thread will **degrade UX**.

### URL origin

Which of the URLs below have the same "origin" as https://mobile.ibm.com? Select all that apply.

http://mobile.ibm.com

https://mobile.ibm.com/top.html

https://mobile.ibm.net

A: B

### JQuery.AJAX vs XHR

There is no major difference aside from syntactical sugar.

XMLHttpRequest is the raw browser object that jQuery wraps into a more usable and simplified form and cross browser consistent functionality. All jQuery functions use XMLHttpRequest object in the background, but provide additional functionality that you don't have to do yourself.

### XMLHttpRequest

✅ The XMLHttpRequest object can be used to upload a file.

✅ Synchronous XMLHttpRequest() has been deprecated.

❌ The web browser displays a visual progress indicator while the XMLHttpRequest is being processed.

 Variable available to us inside the xhttp.onreadystatechange callback in order to check the state of our request:  `this.readyState`, `this.status`, `this.statusText`, `this.responseXML`, `this.reponseText`

> 其中前三个得check。多选题选择项如果是前三个的话就都选

![image-20250501141115527](/Users/lesley/Documents/USC/CSCI571/pastPapers/pics/AJAX_xhr_checkcallback.png)

❌ To request CORS, with XMLHttpRequest, the client JavaScript must issue an Origin header.

### fetch() API

✅ Provides a more powerful and flexible feature set than XMLHttpRequest()

- * fetch() is **modern, promise-based**, and easier to use.
  * It supports **streaming, async/await**, and more straightforward syntax for chaining responses.
  * Cleaner and less verbose than XMLHttpRequest.

❌  It is identical to jQuery’s .ajax()

- While both send HTTP requests, fetch() is **not identical**:
  - .ajax() is a **jQuery wrapper** with its own options, events, and behaviors.
  - fetch() uses **native Promises** and doesn’t auto-parse JSON or auto-handle things like timeouts or error states the same way.

❌  Unlike jQuery ajax(), cannot set CORS mode

- - fetch() **does support CORS** and gives **explicit control** over it.

  - You can set:

    ```js
    fetch(url, {
      mode: 'cors' // or 'no-cors', 'same-origin'
    });
    
    ```

  * So fetch() actually offers **more direct CORS handling** than jQuery .ajax().

❌  The fetch() API can receive cross-site cookies.



### CORS

✅ Images do not have cross-domain issues.

✅ CORS and server proxy are good ways to avoid cross-domain browser restrictions.

### Ajax Application Characteristics

– **Single Page**

– Smooth, continuous User Interaction

– Interactive Elements

– **"Live" content**

– **Visual Effects**

– Animations, **dynamic icons**

– Single keystrokes can lead to server calls

– New Widgets (selectors, buttons, tabs, lists)

– New Styles of Interaction (drag-and-drop, keyboard shortcuts, double-click)

### Qs

✅ **Netscape 7** and **Mozilla Firefox 1.0** were the first browsers to "clone" XMLHttpRequest functionality from Internet Explorer.

✅ Fonts on a web page may be requested across domains using CORS.



## High Performance Websites

### rules

1. Make fewer HTTP requests

   1. Methods:
      – Combine scripts
      – Combine style sheets
      – Combine images into an image map

2. Use a CDN (content distribution network)

3. Add an Expires header

4. Gzip components

5. Put stylesheets at the top

   1. Use <link> (not @import)

   2. Link to a stylesheet for a specific page, but import a stylesheet that applies to

      all pages

6. Move scripts to the bottom

7. ~~Avoid CSS expressions (obsolete)~~

8. Make JS and CSS external

9. Reduce DNS lookups

10. Minify JS & CSS

11. Avoid redirects

12. Remove duplicate scripts

13. Configure Etags

14. Make AJAX cacheable

Newer Rules:

15. Avoid empty src or href
16. Use GET for AJAX requests, avoid POST
17. Reduce the number of DOM elements
18. Avoid HTTP 404 (Not Found) error
19. Reduce Cookie size
20. Use cookie-free domains
21. Do not scale images in HTML
22. Make favicon small and cacheable



The types of files should be compressed to improve web site performance:

* scripts: Minified JavaScript files, Non-minified JavaScript files, text files
* Stylesheets
* XML, JSON, JSONP 
* ❌ not images(png, jpg)
* ❌ not PDF

#### The Performance Golden Rule

The Performance Golden Rule is that 80%-90% is spent on the front-end. Therefore you should start there because\_\_\_\_\_\_ . Select all that apply.

❌ A) ... it is simpler to optimize

❌ B) ... it has proven to work

❌ C) ... it has great potential for improvement

❌ D) ... Wilfredo Pareto Principle says so

✅ E) ... it is much cheaper than changing back end



* What is the most important rule for improving web site performance?

​		**Compress components**



## JQuery

Objects abstracted by jQuery: **JSON**; **XMLHttpRequest**; **DOM**

jQuery is not needed when DOM manipulation is not used.

jQuery has fairly **complex** **ajax** support functions.

Q:

`$("input[value='Hot Fuzz'] ").text( "Hot Fuzz" ) ;` This is a attribute equals selector

## Web Security

* Techniques used to bypass the same-origin policy:

​		✅ Browser extensions

​		✅ CORS

​		✅ JSONP

​		❌ XMLHttpRequest

​		❌ FRAME tag

​		❌ VIDEO tag

​		✅ Browser plugins

​		✅ The Dynamic Script Tag



* .onion is the special-use TLD used in the "deep web"

* The major reason to deprecating V2 Onion Service is exposure to

  attacks.

* v2 Onion Service addresses were deprecated because of safety.



❌ Combining VPN and TOR makes a user much more easily traceable.

Reason: Combining anonymizing VPN + Tor adds an extra layer of encryption and anonymity making it virtually impossible to trace you.



* Which types of hacks can cause damage to the user on the client side? Select all that apply.

  ✅ Log user keystrokes

  ✅ Stealing cookies

  ❌ Denial of Service

  ✅ Install malicious software

  ❌ Deface pages, altering content

* Which of the following are **client-side** attacks? Select all that apply.

  ✅ Clickjacking

  ❌ Insufficient Authentication

  ✅ Browser and Plugin vulnerability

  ✅ Cross-site scripting (XSS)

  ❌ Cross-Site Request Forgery (CSRF) ‼️  reason: It targets the server

*  Which of the following are **authentication** attacks?

  ❌ Content Spoofing

  ❌ Cross-Site Request Forgery (CSRF)

  ✅ Weak Password Recovery Validation

  ✅ Insufficient Authentication

  ✅ Brute Force Attacks

* Which of the following are **Injection** Attacks?

  ✅ Cross Site Request Forgery (CSRF)

  ✅ Search Worms

  ❌ Content Spoofing

  ✅ SQL Injection

  ❌ DDoS attack

* What are true statements of "Diceware" generated passwords?

  ✅ Creates passwords that are extremely secure

  ✅ Creates passwords that are easy to memorize

* JSON array is vulnerable to: Javascript Hijacking
* 