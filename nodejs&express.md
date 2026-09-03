# Node.js & Express.js Interview Questions — All 30, Combined

---

*Questions 1–15: Node.js | Questions 16–30: Express.js*

## 1. Explain the Node.js event loop architecture in detail.

### সহজভাবে বুঝি
Node.js-এর Event Loop asynchronous এবং non-blocking কাজ handle করে।

সহজ flow:
JavaScript → Call Stack → Async Operation → Event Loop → Callback

JavaScript code Call Stack-এ run করে। কোনো asynchronous operation হলে Node.js সেটি background-এ handle করে। কাজ শেষ হলে callback ready হয় এবং Event Loop সেটি execute করে।

### বাংলা Interview Answer
Node.js Event Loop asynchronous এবং non-blocking operation handle করতে সাহায্য করে। JavaScript code Call Stack-এ run করে। Asynchronous কাজ Node.js APIs এবং libuv handle করে। কাজ শেষ হলে callback ready হয় এবং Event Loop সেটি execute করে। Event Loop-এর প্রধান phases হলো Timers, Pending Callbacks, Poll, Check এবং Close Callbacks।

### English Interview Answer
The Node.js Event Loop helps handle asynchronous and non-blocking operations. JavaScript code runs on the Call Stack. Asynchronous operations are handled by Node.js APIs and libuv. When the operation is completed, the callback becomes ready and the Event Loop executes it. The main phases of the Event Loop are Timers, Pending Callbacks, Poll, Check, and Close Callbacks.

---

## 2. What is the difference between process.nextTick(), setImmediate(), and setTimeout()?

### সহজভাবে বুঝি
এই তিনটি function পরে code execute করার জন্য ব্যবহার করা হয়।
- process.nextTick() → current code শেষ হওয়ার পর খুব দ্রুত execute হয়
- setTimeout() → Timers phase-এ delay-এর পরে execute হয়
- setImmediate() → Check phase-এ execute হয়

### বাংলা Interview Answer
process.nextTick() current synchronous code শেষ হওয়ার পর খুব দ্রুত execute হয়। setTimeout() Timers phase-এ given delay-এর পরে execute হয়। আর setImmediate() Event Loop-এর Check phase-এ execute হয়।

### English Interview Answer
process.nextTick() runs very soon after the current synchronous code finishes. setTimeout() runs in the Timers phase after the given delay. And setImmediate() runs in the Check phase of the Event Loop.

---

## 3. How does Node.js handle asynchronous operations internally?

### সহজভাবে বুঝি
Node.js asynchronous operation-এর জন্য main JavaScript thread block করে না।

সহজ flow:
JavaScript → Node.js API → libuv → OS/Thread Pool → Event Loop → Callback

### বাংলা Interview Answer
Node.js asynchronous operation handle করার সময় main JavaScript thread block করে না। Operation Node.js APIs এবং libuv-এর মাধ্যমে handle হয়। কিছু operation OS বা libuv thread pool handle করে। Operation শেষ হলে Event Loop callback execute করে।

### English Interview Answer
Node.js does not block the main JavaScript thread while handling asynchronous operations. The operation is handled through Node.js APIs and libuv. Some operations are handled by the OS or libuv thread pool. When the operation is completed, the Event Loop executes the callback.

---

## 4. Explain the role of libuv in Node.js.

### সহজভাবে বুঝি
libuv হলো Node.js-এর একটি important library, যা asynchronous operation এবং Event Loop handle করতে সাহায্য করে।

### বাংলা Interview Answer
libuv হলো একটি library, যা Node.js-এর asynchronous operation handle করতে সাহায্য করে। এটি Event Loop, networking, timers, file system এবং thread pool-এর সাথে কাজ করে। এর মাধ্যমে Node.js non-blocking I/O support করতে পারে।

### English Interview Answer
libuv is a library that helps Node.js handle asynchronous operations. It works with the Event Loop, networking, timers, the file system, and the thread pool. It helps Node.js support non-blocking I/O.

---

## 5. What are streams in Node.js? Explain different stream types.

### সহজভাবে বুঝি
Stream পুরো data একসাথে memory-তে load না করে ছোট ছোট chunk হিসেবে process করে।

Node.js-এ চার ধরনের main stream আছে:
- Readable
- Writable
- Duplex
- Transform

### বাংলা Interview Answer
Stream হলো এমন একটি mechanism, যা পুরো data একসাথে memory-তে load না করে ছোট ছোট chunk হিসেবে process করতে দেয়। Node.js-এ চার ধরনের main stream আছে। Readable stream data read করে, Writable stream data write করে, Duplex stream read এবং write দুটোই করে, আর Transform stream data read ও write করার পাশাপাশি data modify করতে পারে।

### English Interview Answer
A Stream is a mechanism that allows us to process data in small chunks instead of loading the entire data into memory. Node.js has four main types of streams. Readable streams read data, Writable streams write data, Duplex streams can read and write data, and Transform streams can read, write, and modify data.

---

## 6. How would you handle large file uploads efficiently in Node.js?

### সহজভাবে বুঝি
Large file পুরোটা memory-তে load করা উচিত না। Stream ব্যবহার করে file-কে ছোট ছোট chunk হিসেবে process করা উচিত।

### বাংলা Interview Answer
Large file upload handle করার সময় আমি পুরো file memory-তে load করি না। আমি Streams ব্যবহার করে file-কে ছোট ছোট chunk হিসেবে process করি। প্রয়োজনে file storage service ব্যবহার করি এবং upload size ও file type validate করি। এতে memory usage কম থাকে এবং performance ভালো থাকে।

### English Interview Answer
When handling large file uploads, I do not load the entire file into memory. I use Streams to process the file in small chunks. If needed, I use a file storage service and validate the upload size and file type. This keeps memory usage low and improves performance.

---

## 7. What is backpressure in streams and how do you solve it?

### সহজভাবে বুঝি
যখন Readable stream data produce করার speed Writable stream-এর processing speed-এর চেয়ে বেশি হয়, তখন backpressure হয়।

### বাংলা Interview Answer
Backpressure তখন হয় যখন Readable stream data produce করার speed Writable stream-এর processing speed-এর চেয়ে বেশি হয়। এতে memory-তে বেশি data জমতে পারে। এটি handle করার জন্য আমি stream-এর flow control করি এবং pipe() বা async iteration ব্যবহার করি। এতে data producer এবং consumer-এর speed balance করা যায়।

### English Interview Answer
Backpressure happens when a Readable stream produces data faster than a Writable stream can process it. This can cause too much data to build up in memory. To handle it, I control the stream flow and use pipe() or async iteration. This helps balance the speed between the producer and consumer.

---

## 8. Explain clustering in Node.js. When should you use it?

### সহজভাবে বুঝি
একটি Node.js process সাধারণত একটি main CPU core ব্যবহার করে।

Cluster ব্যবহার করে multiple worker process তৈরি করা যায়, যাতে multiple CPU core ব্যবহার করা সম্ভব হয়।

### বাংলা Interview Answer
Node.js-এর একটি process সাধারণত একটি main CPU core ব্যবহার করে। Clustering ব্যবহার করে আমরা multiple worker process তৈরি করতে পারি। এতে application multiple CPU core ব্যবহার করতে পারে এবং high traffic handle করতে পারে। এটি CPU resources বেশি ব্যবহার করার প্রয়োজন হলে বা server scaling-এর ক্ষেত্রে ব্যবহার করা যায়।

### English Interview Answer
A Node.js process usually uses one main CPU core. With clustering, we can create multiple worker processes. This allows the application to use multiple CPU cores and handle high traffic. It can be useful when we need to use more CPU resources or scale a server.

---

## 9. Difference between worker threads and cluster module?

### সহজভাবে বুঝি
Cluster → Multiple processes
Worker Threads → Multiple threads inside a process

Cluster mainly server scaling-এর জন্য useful, আর Worker Threads CPU-intensive কাজের জন্য useful।

### বাংলা Interview Answer
Cluster multiple process তৈরি করে এবং mainly server scale করার জন্য ব্যবহার করা হয়। Worker Threads একই process-এর মধ্যে multiple thread ব্যবহার করে এবং CPU-intensive কাজ handle করার জন্য useful।

### English Interview Answer
The Cluster module creates multiple processes and is mainly used to scale a server. Worker Threads use multiple threads inside the same process and are useful for handling CPU-intensive tasks.

---

## 10. How does Node.js achieve non-blocking I/O?

### সহজভাবে বুঝি
I/O operation শুরু হলে Node.js তার জন্য wait করে না। এটি অন্য কাজ করতে থাকে।

### বাংলা Interview Answer
Node.js Event Loop এবং libuv ব্যবহার করে non-blocking I/O achieve করে। I/O operation শুরু হলে Node.js wait করে না। এটি অন্য JavaScript code execute করতে থাকে। I/O operation শেষ হলে Event Loop result বা callback handle করে।

### English Interview Answer
Node.js achieves non-blocking I/O using the Event Loop and libuv. When an I/O operation starts, Node.js does not wait for it. It continues executing other JavaScript code. When the I/O operation is completed, the Event Loop handles the result or callback.

---
<!-- 
## 11. Explain CommonJS vs ES Modules in Node.js.

### সহজভাবে বুঝি
দুটিই JavaScript module system।

CommonJS: require() + module.exports
ES Modules: import + export

### বাংলা Interview Answer
CommonJS-এ require() এবং module.exports ব্যবহার করা হয়। ES Modules-এ import এবং export ব্যবহার করা হয়। ES Modules হলো modern JavaScript standard এবং modern Node.js application-এ এটি commonly used হয়।

### English Interview Answer
CommonJS uses require() and module.exports. ES Modules use import and export. ES Modules are the modern JavaScript standard and are commonly used in modern Node.js applications.

---

## 12. What are memory leaks in Node.js and how do you debug them?

### সহজভাবে বুঝি
যখন application আর প্রয়োজন নেই এমন memory release করে না, তখন memory leak হয়।

সময় যাওয়ার সাথে memory usage বাড়তে পারে এবং application slow বা crash করতে পারে।

### বাংলা Interview Answer
Memory leak তখন হয় যখন application আর প্রয়োজন নেই এমন memory release করে না। এটি debug করার জন্য আমি Node.js Inspector এবং Chrome DevTools ব্যবহার করে heap snapshot নিতে পারি। এরপর snapshot compare করে কোন object unnecessary memory ধরে রাখছে তা check করি। এছাড়া timers, event listeners, global variables এবং caches check করি।

### English Interview Answer
A memory leak happens when an application does not release memory that it no longer needs. To debug it, I can use Node.js Inspector and Chrome DevTools to take heap snapshots. Then I compare the snapshots to find which objects are holding unnecessary memory. I also check timers, event listeners, global variables, and caches.

---

## 13. How would you optimize a slow Node.js application?

### সহজভাবে বুঝি
প্রথমে slow হওয়ার কারণ বা bottleneck খুঁজে বের করতে হবে। তারপর সেই জায়গা optimize করতে হবে।

### বাংলা Interview Answer
প্রথমে আমি profiling বা monitoring ব্যবহার করে bottleneck খুঁজে বের করি। এরপর database query optimize করি, unnecessary synchronous operation কমাই, caching ব্যবহার করি এবং CPU-intensive কাজের জন্য Worker Threads ব্যবহার করি। এছাড়া memory leak এবং response size check করি।

### English Interview Answer
First, I find the bottleneck using profiling or monitoring. Then I optimize database queries, reduce unnecessary synchronous operations, use caching, and use Worker Threads for CPU-intensive tasks. I also check for memory leaks and large response sizes.

---

## 14. Explain event emitters with practical use cases.

### সহজভাবে বুঝি
EventEmitter custom event তৈরি এবং handle করতে ব্যবহার করা হয়।

on() → event listen করে
emit() → event trigger করে

যেমন user registration-এর পরে welcome email পাঠানোর মতো কাজ event দিয়ে handle করা যায়।

### বাংলা Interview Answer
EventEmitter হলো Node.js-এর একটি mechanism, যা custom event তৈরি এবং handle করতে ব্যবহার করা হয়। on() দিয়ে event listen করা হয় এবং emit() দিয়ে event trigger করা হয়। এটি notifications, logging, user registration এবং background tasks-এর মতো use case-এ ব্যবহার করা যায়।

### English Interview Answer
EventEmitter is a mechanism in Node.js used to create and handle custom events. We use on() to listen for an event and emit() to trigger an event. It can be used for notifications, logging, user registration, and background tasks.

---

## 15. What happens internally when you run npm install?

### সহজভাবে বুঝি
npm install চালালে npm project-এর dependencies check করে এবং প্রয়োজনীয় packages install করে।

### বাংলা Interview Answer
npm install চালালে npm প্রথমে package.json থেকে dependencies পড়ে। এরপর dependency versions resolve করে, packages download করে এবং node_modules folder-এ install করে। package-lock.json থাকলে npm সেটি use করে consistent dependency versions install করতে পারে।

### English Interview Answer
When we run npm install, npm first reads the dependencies from package.json. Then it resolves the dependency versions, downloads the packages, and installs them into the node_modules folder. If package-lock.json exists, npm can use it to install consistent dependency versions.

---

# 🟢 EXPRESS.JS INTERVIEW QUESTIONS

## 16. Explain the Express.js request-response lifecycle.

### সহজভাবে বুঝি
একটি Express request সাধারণত এই flow follow করে:
Request → Middleware → Route → Controller → Service/Database → Response

### বাংলা Interview Answer
Express.js-এ client থেকে request আসার পর প্রথমে middleware execute হয়। এরপর matching route পাওয়া যায় এবং controller request handle করে। প্রয়োজন হলে controller service বা database-এর সাথে কাজ করে। শেষে server client-কে response পাঠায়।

### English Interview Answer
In Express.js, when a request comes from the client, the middleware runs first. Then Express finds the matching route and the controller handles the request. If needed, the controller works with the service or database. Finally, the server sends a response to the client.

---

## 17. What is middleware in Express.js?

### সহজভাবে বুঝি
Middleware হলো এমন function, যা request এবং response-এর মাঝখানে কাজ করে।

যেমন:
- Authentication
- Validation
- Logging
- Error handling

### বাংলা Interview Answer
Express.js-এ middleware হলো এমন একটি function, যা request এবং response-এর মাঝখানে কাজ করে। এটি authentication, validation, logging এবং error handling-এর মতো কাজে ব্যবহার করা হয়। next() ব্যবহার করে request-কে পরের middleware বা route-এ পাঠানো যায়।

### English Interview Answer
In Express.js, middleware is a function that runs between the request and the response. It is used for authentication, validation, logging, and error handling. We can use next() to pass the request to the next middleware or route.

---

## 18. Difference between application-level, router-level, and error-handling middleware?

### সহজভাবে বুঝি
Application-level → পুরো application-এর জন্য
Router-level → specific router বা route group-এর জন্য
Error-handling → error handle করার জন্য

### বাংলা Interview Answer
Application-level middleware পুরো application-এর জন্য কাজ করে। Router-level middleware specific router বা route group-এর জন্য কাজ করে। Error-handling middleware application-এর error handle করার জন্য ব্যবহার করা হয়।

### English Interview Answer
Application-level middleware works across the application. Router-level middleware works for a specific router or group of routes. Error-handling middleware is used to handle application errors.

---

## 19. How does next() work internally?

### সহজভাবে বুঝি
Express middleware এবং route handler-এর একটি stack maintain করে।

next() call করলে Express সেই stack-এর পরের matching middleware বা route handler-এ যায়।

### বাংলা Interview Answer
Express middleware এবং route handler-এর একটি stack maintain করে। যখন next() call করা হয়, Express সেই stack-এর পরের matching middleware বা route handler-এ request পাঠায়। আর next(error) হলে Express normal middleware skip করে error-handling middleware-এ যায়।

### English Interview Answer
Express maintains a stack of middleware and route handlers. When next() is called, Express moves the request to the next matching middleware or route handler in the stack. If next(error) is called, Express skips the normal middleware and moves to the error-handling middleware.

---

## 20. How would you structure a scalable Express.js project?

### সহজভাবে বুঝি
বড় project-এ সব code এক file-এ না রেখে responsibility অনুযায়ী আলাদা folder-এ রাখা হয়।

Example:
```
src/
├── routes/
├── controllers/
├── services/
├── models/
├── middlewares/
├── validators/
├── config/
└── utils/
```

### বাংলা Interview Answer
আমি Express.js project-কে modular structure-এ রাখি। Routes endpoint define করে, controllers request এবং response handle করে, services business logic রাখে, models database logic handle করে এবং middlewares authentication, validation ও error handling-এর জন্য ব্যবহার করি।

### English Interview Answer
I keep the Express.js project in a modular structure. Routes define the endpoints, controllers handle requests and responses, services contain business logic, models handle database logic, and middlewares are used for authentication, validation, and error handling.

---

## 21. Explain REST API best practices in Express.js.

### সহজভাবে বুঝি
একটি ভালো REST API-তে proper HTTP methods, status codes, validation, consistent endpoints এবং security থাকা উচিত।

### বাংলা Interview Answer
REST API design করার সময় আমি proper HTTP methods এবং status codes ব্যবহার করি। API endpoints simple এবং consistent রাখি। User input validate করি এবং errors properly handle করি। Authentication ব্যবহার করে API secure রাখি।

### English Interview Answer
When designing a REST API, I use proper HTTP methods and status codes. I keep the API endpoints simple and consistent. I validate user input and handle errors properly. I also use authentication to keep the API secure.

---

## 22. How do you implement centralized error handling?

### সহজভাবে বুঝি
প্রতিটি route-এ আলাদাভাবে error handle না করে একটি centralized error-handling middleware ব্যবহার করা যায়।

### বাংলা Interview Answer
আমি একটি centralized error-handling middleware তৈরি করি এবং application-এর শেষে রাখি। কোনো route বা middleware-এ error হলে next(error) ব্যবহার করে সেই error central handler-এ পাঠাই। তারপর সেখানে proper status code এবং error message দিয়ে response পাঠাই। এতে সব error এক জায়গায় handle করা যায়।

### English Interview Answer
I create a centralized error-handling middleware and place it at the end of the application. When an error occurs in a route or middleware, I use next(error) to send the error to the central handler. Then I send the response with a proper status code and error message. This allows me to handle all errors in one place.

---

## 23. How do you validate incoming request data?

### সহজভাবে বুঝি
Client থেকে আসা data সঠিক কিনা check করাই validation।

যেমন:
- Required field আছে?
- Email ঠিক আছে?
- Password ঠিক format-এর?
- Data type সঠিক?

### বাংলা Interview Answer
আমি validation middleware ব্যবহার করে incoming request data validate করি। আমি check করি required fields আছে কিনা এবং data type ও format সঠিক কিনা। যদি data invalid হয়, তাহলে request reject করে proper error response পাঠাই। Valid হলে request-কে পরের middleware বা controller-এ পাঠাই।

### English Interview Answer
I use validation middleware to validate incoming request data. I check if the required fields are present and if the data type and format are correct. If the data is invalid, I reject the request and send a proper error response. If it is valid, I pass the request to the next middleware or controller.

---

## 24. Explain route modularization in Express.js.

### সহজভাবে বুঝি
সব route একটি বড় file-এ না রেখে আলাদা router file-এ ভাগ করাই route modularization।

যেমন:
```
routes/
├── user.routes.js
├── product.routes.js
└── order.routes.js
```

### বাংলা Interview Answer
Route modularization হলো application-এর routes আলাদা আলাদা router file-এ ভাগ করা। এতে code organized, reusable এবং maintain করা সহজ হয়।

### English Interview Answer
Route modularization means separating application routes into different router files. It keeps the code organized, reusable, and easier to maintain.

---

## 25. Difference between authentication and authorization?

### সহজভাবে বুঝি
Authentication → আপনি কে?
Authorization → আপনি কী করতে পারবেন?

যেমন:
Login → Authentication
Admin-only access → Authorization

### বাংলা Interview Answer
Authentication হলো user কে verify করা বা user কে চেনা। Authorization হলো সেই user কী কী করতে পারবে তা check করা।

### English Interview Answer
Authentication means verifying who the user is. Authorization means checking what the user is allowed to do.

---

## 26. How do you implement role-based access control (RBAC)?

### সহজভাবে বুঝি
RBAC-এর full form হলো Role-Based Access Control।

User-এর role অনুযায়ী permission দেওয়া হয়।

যেমন:
Admin → Create, Update, Delete
User → View

### বাংলা Interview Answer
RBAC বা Role-Based Access Control হলো এমন একটি access control system, যেখানে user-এর role অনুযায়ী permission দেওয়া হয়। প্রথমে user-এর role database-এ রাখি এবং authentication-এর মাধ্যমে user verify করি। এরপর role-based middleware check করে user এই route access করতে পারবে কিনা। Allowed হলে next() করি, না হলে 403 Forbidden response পাঠাই।

### English Interview Answer
RBAC or Role-Based Access Control is an access control system where permissions are given based on the user's role. First, I store the user's role in the database and verify the user through authentication. Then a role-based middleware checks whether the user can access the route. If allowed, I call next(). Otherwise, I send a 403 Forbidden response.

---

## 27. How would you secure an Express.js API?

### সহজভাবে বুঝি
API secure করার জন্য authentication, authorization, validation, HTTPS, rate limiting এবং secure headers ব্যবহার করা যায়।

### বাংলা Interview Answer
আমি authentication এবং authorization ব্যবহার করে API secure করি। User input validate করি এবং HTTPS ব্যবহার করি। বেশি request আটকানোর জন্য rate limiting ব্যবহার করি। এছাড়া secret keys .env file-এ রাখি এবং secure headers ব্যবহার করি।

### English Interview Answer
I secure the API by using authentication and authorization. I validate user input and use HTTPS. I use rate limiting to prevent too many requests. I also keep secret keys in the .env file and use secure headers.

---

## 28. Explain CORS and common issues developers face with it.

### সহজভাবে বুঝি
CORS হলো browser-এর security mechanism, যা different origin-এর মধ্যে request control করে।

Common issues:
- Wrong origin
- Credentials configuration
- Methods বা headers allow না করা

### বাংলা Interview Answer
CORS হলো browser-এর একটি security system, যা different origin-এর মধ্যে request control করে। CORS ঠিকভাবে configure না করলে browser request block করতে পারে। Common problem হলো wrong origin, credentials এবং methods বা headers ঠিকভাবে allow না করা।

### English Interview Answer
CORS is a browser security system that controls requests between different origins. If CORS is not configured properly, the browser can block the request. Common problems are wrong origin, credentials, and not allowing the required methods or headers.

---

## 29. How do cookies and sessions work in Express.js?

### সহজভাবে বুঝি
Cookie → Browser-এ থাকে
Session → Server-এ থাকে

Flow:
Login → Server creates session → Session ID → Cookie → Browser

### বাংলা Interview Answer
Express.js-এ cookie browser-এ ছোট data রাখে, আর session server-side-এ user-এর information রাখে। User login করলে server একটি session তৈরি করে এবং session ID cookie-তে পাঠায়। এরপর browser প্রতিটি request-এর সাথে সেই cookie পাঠায়। Server session ID ব্যবহার করে user-কে চিনতে পারে।

### English Interview Answer
In Express.js, a cookie stores small data in the browser, while a session stores user information on the server. When a user logs in, the server creates a session and sends the session ID in a cookie. Then the browser sends the cookie with each request. The server uses the session ID to identify the user.

---

## 30. Difference between stateless and stateful authentication?

### সহজভাবে বুঝি
Stateless → Server session store করে না → JWT
Stateful → Server session store করে → Session ID

### বাংলা Interview Answer
Stateless authentication-এ server user-এর session information store করে না। সাধারণত JWT token ব্যবহার করা হয় এবং প্রতিটি request-এর সাথে token পাঠানো হয়। Stateful authentication-এ server user-এর session store করে এবং browser session ID cookie হিসেবে পাঠায়।

### English Interview Answer
In stateless authentication, the server does not store the user's session information. Usually, a JWT token is used and sent with each request. In stateful authentication, the server stores the user's session and the browser sends the session ID as a cookie. -->