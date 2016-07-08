+++
date = "2016-07-08T13:08:42-04:00"
next = "/week6/day28"
prev = "/week6/day27"
title = "Day 28: User Authentication"
toc = true
weight = 4

+++

<date>Friday, July 8, 2016</date>

## Topics

### bcrypt
bcrypt is a password hashing function based on the Blowfish cipher, developed in 1999.  

#### Key features
  * It is an **adaptive function**, meaning the iteration count can be increased to counteract increases in computing power.  As computers get more powerful, the difficulty of reversing the encryption can be increased.
  * Utilizes a **salt**, random data used as an additional input to a hashing function.  This helps prevent [rainbow-table attacks](https://en.wikipedia.org/wiki/Rainbow_table) - attacks using a pre-computed table for reversing cryptographic hash functions.
  * Identify bcrypt hashes easily - they all start with "$2a$", "$2b$", or "$2y$"

  {{% notice tip %}}
  Never, EVER store plain-text user passwords in your database. Always encrypt.   Read [Storing user passwords securely: hashing, salting, and bcrypt](http://dustwell.com/how-to-handle-passwords-bcrypt.html) for a great explanation.
  {{% /notice %}}

### [bcryptjs](https://www.npmjs.com/package/bcryptjs)
Optimized bcrypt in plain JavaScript with zero dependencies

How to get started:

```sh
npm install bcryptjs
```
```js
var bcrypt = require('bcryptjs');
var salt = bcrypt.genSaltSync(10); // parameter is the number of rounds to use
var hash = bcrypt.hashSync('plain_text_password', salt);
```

## Projects

Meganote:  [Source](https://github.com/xternbootcamp16/meganote/tree/e527d75025d4357af527f47adc652b7acb396f2c)

Meganote-server: [Source](https://github.com/xternbootcamp16/meganote-server/tree/f1b26abb35938831bddcfaed45307f041d99a047)


## Homework

User authentication and persistence in Meganote

#### Base Requirements
If user is signed out, display a link to 'Sign Up' in the navbar

If user is signed in, display a link to 'Sign Out' instead (and have it work). Also, display the current user's name in the navbar

#### Super Mega Bonus Credit
Use custom directives to fulfill the base requirements

#### Super Mega Bonus Credit Hyper Fighting
Create a working profile page where you can update a user's profile
