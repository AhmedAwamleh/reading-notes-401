# NodeJS, Express, TDD, CI/CD

**[Return to Main Page](https://annethor.github.io/reading-notes/)**

## What’s the difference between PUT and PATCH? (HTTP verbs)

PATCH and PUT are both methods that apply modifications to an existing resource. The difference is that PATCH is a *partial* modification of the resource and PUT is a *total replacement* of the existing resource or *creation* of the resource. Another important difference is that calling PUT repeatedly will always yield the same result with no side effects; repeated calls to PATCH are not guaranteed to do so (ex/if there is an auto increment field in the resource, this may keep incrementing with repeated PATCH calls)

MDN Docs:

**[PATCH](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH)**

**[PUT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT)**

## Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

The purposes of a fake API for development are manifold:

- Tests of the servie you are building must not rely on external resources
- The API could be slow or rate limited (which could incur costs)
- Often developers need to work before the API is ready to be connected

More useful to think about these as "test doubles" than "fakes"

Potentially useful mock API services for development:

- [json-server](https://www.npmjs.com/package/json-server)
- [mirage-js](https://miragejs.com/docs/getting-started/introduction/)
- [jest](https://www.npmjs.com/package/jest)
*Note with Jest you would be using ```jest.spyOn``` and ```Fetch``` in testing along with your own version of the Fetch call to evaluate the functionality*
- [JSON Schema Faker](https://github.com/json-schema-faker/json-schema-faker)
- [fake{JSON}](https://fakejson.com/)

**[How To: Rapid Development Via Mock APIS](https://www.freecodecamp.org/news/rapid-development-via-mock-apis-e559087be066/)**

[4 Ways to Fake an API](https://www.valentinog.com/blog/fake/)

## Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

**[Swagger](https://swagger.io/docs/specification/describing-responses/)** allows you define the range of responses as 1XX, 2XX, ...5XX. If you provide the explicit code (i.e. 404) that will take precedence over the blanket request (in this case 4XX). Each response status requires a description. API specs do not necessarily need to cover all possible codes, but known error codes like 404 must be addressed.

**[APIDOC.js](https://apidocjs.com/)** you can also define the errors in groups, if you do not provide the specific code the default error ```Error 4xx``` is thrown. You can set the title and description of the errror with ```@apiDefine```

## Compare and contrast SOAP and ReST

**[SOAP (Simple Object Access Protocol)](https://en.wikipedia.org/wiki/SOAP)**
SOAP uses XML data in request/response messages, relying on XML Schema and other technology to enforce/parse structure of messages. It is platform indepedent (i.e. clients can use from disparate OS). SOAP is extensible, neutral, and independent of specific programming models.

**[REST (Representational State Transfer)](https://en.wikipedia.org/wiki/Representational_state_transfer)**
Standard software architecture for web services. This is a webservice that provides it's web services in a text form allowing them to be read and modified with a stateless protocol and predefined operations. Common, stateless protocols allow for operability amongs disparate OS.

REST has become the more popular communication protocol. REST accesses data whereas SOAP performs operations by a standardized set of messaging patterns. Each are scalable and either can be used to achieve most outcomes. Benefits to REST include: not restricted to XML formatting, JSON is faster and provides a uniform base for transferring data to browser clietns, used by major services like Google, generally faster. Since either can be used to acheive the same results, the preference is up to the developer with the ultimate end goal in mind. SOAP can be preferable due to more robust security guarantees, built in logic to handle failed communications, and a set of standardized processes that make it easier to implement across firewalls/proxies without needing to modify the protocols themselves.

## Reference Terms

Term | Definition
----- | -----------
Web Server | System of one or more computers that accepts incoming HTTP requests and sends corresponding HTTP responses; primary function is to deliver web contents/resources to the client (requestor). "Web Server" can refer to the hardware (computer storing web resources and software) or the software itself(that controls how users interact with hosted files, minimum functionality HTTP)
Node | Open source runtime environment allowing for developers to create server side applications in JavaScript
Express | Express is a Node framework that simplifies HTTP verbs and allows for concise creation of HTTP verb handlers, simple integration with different view engines (i.e. porting information into front end templates), creates common settings such as port to use for connecting, and allows for additional request processing (middleware) to be inserted into request handling. It is unopinionated, meaning that you can structure it in various ways and use many different middleware options in myriad configurations.
Routing | Routing is how the client request is connected to the code they will receive
Web Request Response Cycle (WRRC) | This is how information flows through a web app: client opens brower/enters url, request gets sent to the server which takes the url request, server follows it's routing to serve back the requested web document and passes it to the view, the view renders the information in the desired format back to the client in their browser
