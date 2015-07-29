---
layout: post
title: "HTTP Server Error Status Codes"
categories: articles
share: true
comments: true
tag: [http]
---

HTTP response codes which are within range 500-599 are called HTTP Server Error Status Codes.

Sometimes a client sends a valid request, but the server itself has an error. This could be a client running into a limitation of the server or an error in one of the server’s subcomponents, such as a gateway resource.

Following table shows the various server error status codes.

| Code  | Reason | Meaning  |
| ------------- | ------------- | ------------- |
| 500  | Internal Server Error  | Used when the server encounters an error that prevents it from servicing the request. |
| 501  | Not Implemented  | Used when a client makes a request that is beyond the server’s capabilities (e.g., using a request method that the server does not support). |
| 502  | Bad Gateway  | Used when a server acting as a proxy or gateway encounters a bogus response from the next link in the request response chain (e.g., if it is unable to connect to its parent gateway). |
| 503  | Service Unavailable  | Used to indicate that the server currently cannot service the request but will be able to in the future. If the server knows when the resource will become available, it can include a Retry-After header in the response. |
| 504  | Gateway Timeout  | Similar to status code 408, except that the response is coming from a gateway or proxy that has timed out waiting for a response to its request from another server. |
| 505  | HTTP Version Not Supported  | Used when a server receives a request in a version of the protocol that it can’t or won’t support. Some server applications elect not to support older versions of the protocol. |
