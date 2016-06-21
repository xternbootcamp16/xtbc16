+++
date = "2016-06-21T16:10:52-04:00"
next = "/week4/day16"
prev = "/week4/day15"
title = "Day 16: Firebase and Twilio"
toc = true
weight = 2

+++

<date>Tuesday, June 21, 2016</date>

## Topics

### [Firebase 3.0](https://firebase.google.com/docs/) & [AngularFire 2.0](https://www.firebase.com/docs/web/libraries/angular/api.html)
  * `$firebaseArray` for creating an array-like object that syncs with Firebase
  * `$add`
  * `$remove`
  * `$save`

Firebase 3.0 app initialization for front-end
```js
var config = {
  apiKey: '<your-api-key>',
  authDomain: '<your-auth-domain>',
  databaseURL: '<your-database-url>',
  storageBucket: '<your-storage-bucket>'
};
firebase.initializeApp(config);
```

Firebase 3.0 app initialization for Node.js
```js
var firebase = require("firebase");
firebase.initializeApp({
  serviceAccount: "path/to/serviceAccountCredentials.json",
  databaseURL: "https://databaseName.firebaseio.com"
});
```

### [dotenv](https://github.com/motdotla/dotenv)
  * Loads environment variables from `.env` for nodejs projects
  * Should I commit my `.env` file?  [Answer here](https://github.com/motdotla/dotenv#should-i-commit-my-env-file)

### Twilio
  * Cloud-based communication for text and phone calls
  * Supports multiple server-side SDKs, including Java, C#, Node, Ruby, and Python

Node setup
```js
var twilio = require('twilio');
var client = new twilio.RestClient(accountSid, authToken);

client.messages.create({
    body: 'Hello from Node',
    to: '+12345678901',  // Text this number
    from: '+12345678901' // From a valid Twilio number
}, function(err, message) {
    if(err) {
        console.error(err.message);
    }
});
```

## Project

* Mutant Office Hours (Angular):
[source](https://github.com/xternbootcamp16/mutant-office-hours/tree/330a7770d407cfd22d6e694db439e168d6d230d0)
* Mutant Office Hours Server (Node): [source](https://github.com/xternbootcamp16/mutant-office-hours-server/tree/fa25dc0653b9dba7f94836d88926404f4d4bcbce)
