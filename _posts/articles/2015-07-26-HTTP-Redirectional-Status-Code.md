---
layout: post
title: "HTTP Redirection Status Codes"
categories: articles
share: true
comments: true
tag: [http]
---

HTTP response codes which are within range 300-399 are called HTTP Redirection Status Codes.

The redirection status codes either tell clients to use alternate locations for the resources they’re interested in or provide an alternate response instead of the content. If a resource has moved, a redirection status code and an optional location header can be sent to tell the client that the resource has moved and where it can now be found. This allows browsers to go to the new location transparently, without bothering their human users.

Some of the redirection status codes can be used to validate an application’s local copy of a resource with the origin server. For example, an HTTP application can check if the local copy of its resource is still up-to-date or if the resource has been modified on the origin server. The client sends a special `If-Modified-Since` header saying to get the document only if it has been modified since October 1997. The document has not changed since this date, so the server replies with a 304 status code instead of the contents.

Below is a table which describes various Redirection Status Code.

| Code  | Reason | Meaning  |
| ------------- | ------------- | ------------- |
| 300  | Multiple Choice  | Returned when a client has requested a URL that actually refers to multiple resources, such as a server hosting an English and French version of an HTML document. This code is returned along with a list of options; the user can then select which one he wants. The server can include the preferred URL in the Location header. |
| 301  | Moved Permanently  | Used when the requested URL has been moved. The response should contain in the Location header the URL where the resource now resides. |
| 302  | Found  | Like the 301 status code; however, the client should use the URL given in the location header to locate the resource temporarily. Future requests should use the old URL. |
| 303  | See Other  | Used to tell the client that the resource should be fetched using a different URL. This new URL is in the Location header of the response message. Its main purpose is to allow responses to POST requests to direct a client to a resource.|
| 304  | Not Modified  | Clients can make their requests conditional by the request headers they include. If a client makes a conditional request, such as a GET if the resource has not been changed recently, this code is used to indi- cate that the resource has not changed. Responses with this status code should not contain an entity body.|
| 305  | Use Proxy  | Used to indicate that the resource must be accessed through a proxy; the location of the proxy is given in the Location header. It’s important that clients interpret this response relative to a specific resource and do not assume that this proxy should be used for all requests or even all requests to the server holding the requested resource. This could lead to broken behavior if the proxy mistakenly interfered with a request, and it poses a security hole. |
| 306  | (Unused)  | Not currently used |
| 307  | Temporary Redirect  | Like the 301 status code; however, the client should use the URL given in the location header to locate the resource temporarily. Future requests should use the old URL. |

From table, you may have noticed a bit of overlap between the 302, 303, and 307 status codes. There is some nuance to how these status codes are used, most of which stems from differences in the ways that HTTP/1.0 and HTTP/1.1 applications treat these status codes.
