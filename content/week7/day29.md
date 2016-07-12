+++
date = "2016-07-11T19:00:12-04:00"
next = "/week7/day30"
prev = "/week7/"
title = "Day 29: More User Authentication"
toc = true
weight = 1

+++

<date>Monday, July 11, 2016</date>

## Topics

### bcrypt

We used `bcryptjs` to hash user passwords before storing them in the database for security.  We can also use it to verify that the hash of an incoming plain-text password matches the stored hash.

```js
// Synchronous password checking
bcrypt.compareSync('password_string', stored_password_hash);

// Async password checking
bcrypt.compare('password_string', stored_password_hash, (err, res) => {
  // returns true if password is correct
});
```

### Mongoose

In Mongoose, instances of Models are known as _documents_.  They have many pre-defined instance methods.  Pre-defined instance methods can be overwritten if necessary, or new custom methods can be added.  We have now done both.

First, we overwrote the existing `.toJSON()` method to remove extraneous data from the returned user object.

```js
userSchema.methods.toJSON = function() {
  var user = this.toObject();
  delete user.password;
  delete user.__v;
  return user;
};
```

Later, we wrote a custom `.authenticate()` method for checking to make sure the password was correct before logging in a user.

```js
userSchema.methods.authenticate = function(password, callback) {
  bcrypt.compare(password, this.passwordDigest, (err, isMatch) => {
    callback(isMatch);
  });
};
```

## Projects

Meganote:  [Source](https://github.com/xternbootcamp16/meganote/tree/789d560d632e6da1afcca0c5659e9aa0761ac026)

Meganote-server: [Source](https://github.com/xternbootcamp16/meganote-server/tree/5c622f60cbb7979da752ce66f9ef3898dcad40fb)

## Homework

Show flash messages for the success or failure of 'sign up' and 'log in'

In Meganote Server, re-write the route for logging in using promises
