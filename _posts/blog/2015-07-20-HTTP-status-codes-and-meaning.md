---
layout: post
title: "HTTP Status Code and their meaning"
categories: articles
share: true
comment: true
---

HTTP Status code can be divided into five main categories which are

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

//table take from page 69

## 100-199: Informational Status Code

These are relatively new and were introduced in HTTP/1.1

//table 3.6

There is a little controversy about their usage. For example the 100 Continue Code is intended to optimize the case when client wants to send an entity body to server but wants to check if server can handle that before it starts sending.

Since client, server and proxies may handle these codes in slightly different manner it is generally advised to check documentation if you are planning to use these Status codes.

## 200-299: Success Status Code

To mark success, server has an array of success Status Codes, matched up with different type of requests. Some examples are

// Table 3.7
