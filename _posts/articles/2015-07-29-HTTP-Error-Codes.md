---
layout: post
title: "HTTP Error Status Codes"
categories: articles
share: true
comments: true
tag: [http]
---

HTTP response codes which are within range 400-499 are called HTTP Error Status Codes.

Sometimes a client sends something that a server just can’t handle, such as a badly formed request message or, most often, a request for a URL that does not exist.
We’ve all seen the infamous 404 Not Found error code while browsing. This is just the server telling us that we have requested a resource about which it knows nothing.

Following table shows the various client error status codes.

| Code  | Reason | Meaning  |
| ------------- | ------------- | ------------- |
| 400  | Bad Request  | Used to tell the client that it has sent a malformed request. |
| 401  | Unauthorized  | Returned along with appropriate headers that ask the client to authenticate itself before it can gain access to the resource. |
| 402  | Payment Required  | Currently this status code is not used, but it has been set aside for future use. |
| 403  | Forbidden  | Used to indicate that the request was refused by the server. If the server wants to indicate why the request was denied, it can include an entity body describing the reason. However, this code usually is used when the server does not want to reveal the reason for the refusal. |
| 404  | Not Found  | Used to indicate that the server cannot find the requested URL. Often, an entity is included for the client application to display to the user. |
| 405  | Method not allowed  | Used when a request is made with a method that is not supported for the requested URL. The Allow header should be included in the response to tell the client what methods are allowed on the requested resource. |
| 406  | Not Acceptable  | Clients can specify parameters about what types of entities they are willing to accept. This code is used when the server has no resource matching the URL that is acceptable for the client. Often, servers include headers that allow the client to figure out why the request could not be satisfied. |
| 407  | Proxy Authentication Required  | Like the 401 status code, but used for proxy servers that require authentication for a resource. |
| 408  | Request Timeout  | If a client takes too long to complete its request, a server can send back this sta- tus code and close down the connection. The length of this timeout varies from server to server but generally is long enough to accommodate any legitimate request. |
| 409  | Conflict  | Used to indicate some conflict that the request may be causing on a resource. Servers might send this code when they fear that a request could cause a conflict. The response should contain a body describing the conflict. |
| 410  | Gone  | Similar to 404, except that the server once held the resource. Used mostly for web site maintenance, so a server’s administrator can notify clients when a resource has been removed. |
| 411 | Length Required | Used when the server requires a Content-Length header in the request message. |
| 412 | Precondition Failed | Used if a client makes a conditional request and one of the conditions fails. Conditional requests occur when a client includes an Expect header. |
| 413 | Request Entity Too Large | Used when a client sends an entity body that is larger than the server can or wants to process. |
| 414 | Request URI Too Long | Used when a client sends a request with a request URL that is larger than the server can or wants to process. |
| 415 | Unsupported Media Type  | Used when a client sends an entity of a content type that the server does not understand or support. |
| 416 | Requested Range Not Satisfiable | Used when the request message requested a range of a given resource and that range either was invalid or could not be met. |
| 417 | Expectation Failed | Used when the request contained an expectation in the Expect request header that the server could not satisfy. |
