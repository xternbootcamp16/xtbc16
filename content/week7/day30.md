+++
date = "2016-07-12T15:22:54-04:00"
next = "/week7/day30"
prev = "/week7/day29"
title = "Day 30: Authentication with JWT"
toc = true
weight = 2

+++

<date>Tuesday, July 12, 2016</date>

## Topics

### JSON Web Tokens
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

JWTs are composed of three base-64 strings that are joined together with dot notation.  

`xxxxxxxxxx.yyyyyyyyyyy.zzzzzzzzz`

The first component is the _header_, which contains information about the type of token and the hashing algorithm used to create it.

```js
// decoded header
{
  "alg": "HS256",
  "typ": "JWT"
}
```

The second component is the _payload_, which contains the actual information being sent.

```js
// decoded payload
{
  "title": "The greatest note ever",
  "body_html": "seriously, it is"
}
```

The last component is the _signature_.  To create it, you take the encoded header, encoded payload, specified hashing algorithm, a secret, and sign it.

```js
// method to create a signature
HMACSHA256(
  base64UrlEncode(header) + "." + base64UrlEncode(payload),
  secret)
```

#### Advantages of JWTs
  * Lightweight
  * Self-contained
  * Reduced database queries, since the token contains all of the required information about the user
  * Because information can be signed, you can be confident that the sender is who they say they are, and that the information has not been tampered with

#### Learn more about JSON Web Tokens
  * [Introduction to JSON Web Tokens - jwt.io](https://jwt.io/introduction/)
  * [The Anatomy of a JSON Web Token - scotch.io](https://scotch.io/tutorials/the-anatomy-of-a-json-web-token)
  * [JWT Debugger](https://jwt.io/) - a useful tool for interactively working with JWTs

### Angular Interceptors
Interceptors are used any time it is desirable to intercept requests before they are handed to the server and responses before they are handed off to the application code. They are factories that are added to the `$httpProvider.interceptors` array

In Meganote, we used an interceptor to add JSON Web Tokens to the headers of requests being sent to our API

Read more about interceptors [here](https://docs.angularjs.org/api/ng/service/$http)

## Projects

Meganote:  [Morning](https://github.com/xternbootcamp16/meganote/tree/f2a7deaec6389589ed82c512b5b862a1f53893a2) | [Afternoon](https://github.com/xternbootcamp16/meganote/tree/354ca8350988b43eb95cc695ed995cb52fcc3622)

Meganote-server: [Morning](https://github.com/xternbootcamp16/meganote-server/tree/4b41f89775990101773b3957dc20438125669ca7) | [Afternoon](https://github.com/xternbootcamp16/meganote-server/tree/272530344fc593fcb4edff059160971c04a5425b)

## Homework

Meganote polish!  Add final touches for a better user experience

#### Flash messages
Add flash messages for events like successfully signing in or out, reusing a username, non-matching passwords, etc

#### Better error messages from the server
Enhance the returned JSON responses from the server for better communication with the user

#### Database validation
Enforce database rules on the server side for things like unique usernames and password length

#### Super Mega Bonus Credit
Add a spinner animation that appears while waiting for responses from the API
