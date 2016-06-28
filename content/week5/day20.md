+++
date = "2016-06-27T16:25:11-04:00"
next = "/week5/day21"
prev = "/week5"
title = "Day 20: Mailgun and Firebase Security"
toc = true
weight = 1

+++

<date>Monday, June 27, 2016</date>

## Topics

### Github Pull Requests
  * A request to merge modified code into an existing repository
  * [GitHub Help: Using pull requests](https://help.github.com/articles/using-pull-requests/)
  * [GitHub Help: Commenting on differences between files](https://help.github.com/articles/commenting-on-differences-between-files/)

### Mailgun
  * [mailgun-js](https://www.npmjs.com/package/mailgun-js) - Simple Node.js helper module for Mailgun API
  * [Quickstart Guide](https://documentation.mailgun.com/quickstart.html)

Node mailgun setup
```js
var mailgun = require('mailgun-js');
var mailgunClient = mailgun({ apiKey: MY_API_KEY, domain: MY_DOMAIN });

var emailData = {
  from: 'Example User <user@example.com>',
  to: 'recipient@example.com',
  subject: 'Example Email',
  text: 'This is an email for example purposes'  
};

mailgunClient.messages().send(emailData, function(error, body) {
  console.log(body);
});
```

### Firebase Security
  * Rules are defined in JSON
  * Can define rules in three flavors:
    * `.read` - describes if and when data can be read
    * `.write` - describes if and when data can be written
    * `.validate` - defines correctly formatted values for the data
  * [Security rules cascade](https://www.firebase.com/docs/security/guide/securing-data.html#section-cascade) - child rules can only grant additional privileges, not revoke a read or write privilege.
  * Firebase console has a simulator for testing the security rules that are written
  * [Security Quickstart Guide](https://www.firebase.com/docs/security/quickstart.html)

## Homework
Continue refactor of meganote based on peer feedback on your pull request

## Projects
Mutant Office Hours: [Source](https://github.com/xternbootcamp16/mutant-office-hours/tree/63a93fa014208d11c80fec3f785672c8d2809f43)

Mutant Office Hours Server:
[Source](https://github.com/xternbootcamp16/mutant-office-hours-server/tree/3526b32a5e949b75aaa575d66bbc212e2f71d7cc)
