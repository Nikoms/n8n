---
title: "Distributed Systems with Node.js: Building Enterprise-Ready Backend Services (English"
date: 2025-08-18T23:59:22.980+02:00
category: books
tags: []
excerpt: My highlights
---

## Page 26

> The libuv thread pool size defaults to four, has a max of 1,024, and can be overridden by setting the UV_THREADPOOL_SIZE=<threads> environment variable. In practice it’s not that common to modify it and should only be done after benchmarking the effects in a perfect replication of production. An app running locally on a macOS laptop will behave very differently than one in a container on a Linux server.


----
## Page 35

> For example, if you need to process 1,000 data records, you might consider breaking it up into 10 batches of 100 records, using setImmediate() at the end of each batch to continue processing the next batch.


----
## Page 36

> Don’t introduce Zalgo. When exposing a method that takes a callback, that callback should always be run asynchronously. For example, it’s far too easy to write something like this:


----
## Page 183

> fs.readdir('/proc/self/fd',


----
## Page 183

> setTimeout(() => { statsd.timing('eventlag', begin); }, 0); 2


----
## Page 332

> Be careful when creating singleton instances within an npm package. Consider a package that creates a singleton database connection when it is first instantiated. Depending on how this package has been deduped, it may result in multiple database connections being created in one application. Also, be wary of the instanceof operator


----
## Page 389

> of Node.js v14.8, the --unhandled-rejections=strict flag must be provided for this to crash a process. Future versions of Node.js will crash by default.


----
## Page 395

> Another convention — popularized by Node.js itself — for differentiating errors works by providing a . code property, which is a string named in a documented and consistent manner and that shouldn’t change between releases. An example of this is the ERR_INVALID_URI error code, and even though the human-readable message of the string may change, the error code should not.


----
## Page 398

> Unlike uncaught exceptions, unhandled promise rejections do not cause the process to crash in Node.js v14. In Node.js v15 and above, this will cause the process to exit.


----
## Page 400

> the argument used when emitting an error, such as with EventEmitter#emit('error', arg), should be an instance of the Error class.


----
## Page 401

> SIGUSR1 signal tells Node.js to start the debugger. 3


----
## Page 403

> When a Kubernetes pod is terminated, Kubernetes both stops sending requests to the pod and sends it the SIGTERM signal. Kubernetes also starts a 30 second timer. During this time, the application can then do whatever work is necessary to gracefully shutdown. Once the process is done, it should terminate itself so that the pod will go down. However, if the pod doesn’t terminate itself, Kubernetes will then send it the SIGKILL signal, forcefully closing the application.


----
## Page 406

> encourage you to read Martin Kleppmann’s Designing Data-Intensive Applications


----
## Page 421

> it’s sometimes necessary to prefix the name of a key with a version number to signify the version of the data structure being cached.


----
## Page 462

> Table 8-3. Node.js network errors


----
## Page 463

> Figure 8-5 contains a flowchart that you can follow when designing your own retry logic.


----
## Page 465

> a server may choose to implement the ETag and If-Match HTTP headers to provide additional semantics to avoid data clobbering. 4


----
## Page 466

> mechanism that a server may choose to implement that makes every request idempotent is an idempotency key. An idempotency key is metadata that is provided by the client when making a request to a server.


----
## Page 466

> Consider supporting idempotency keys in your API if the side effect of duplicated requests can be costly.


----
## Page 467

> Circuit Breaker Pattern Sometimes, a message or


----
## Page 468

> Exponential Backoff The naive approach for having a client retry a request to an external service is to simply have it make the request again as soon as the failure happens


----
## Page 470

> Currently, the industry standard is called an exponential backoff. With this approach, the client starts by making retry attempts quickly but then slows down over time.


----
## Page 472

> To overcome this issue, you may want to introduce jitter to your applications. Jitter is random variance, such as an increase or decrease of request timing of ±10%. When this happens, some clients end up quicker and some end up slower.

