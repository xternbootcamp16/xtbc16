+++
date = "2016-07-20T15:56:50-04:00"
next = "/week8/day36"
prev = "/week8/day35"
title = "Day 36: Testing, Partials, Pagination, Devise"
toc = true
weight = 3

+++

<date>Wednesday, July 20, 2016</date>

## Topics

### Testing

Testing is an important part of good software design.  Having a solid suite of tests ensures that your software actually does the things it was designed to do.  More importantly, as your program grows and new features are added and refactored, it ensures that none of the original functionality can be inadvertently compromised.

A popular method in use today is Test Driven Development (TDD).  In TDD, the tests are actually written _before_ the code.  The three steps in TDD are:

  1. Write a failing test
  2. Write enough code to make the test pass
  3. Refactor the code

#### Some testing resources

  * [A Guide to Testing Rails Applications](http://guides.rubyonrails.org/testing.html) - from the Rails docs
  * [Angular Unit Testing](https://docs.angularjs.org/guide/unit-testing) - from the Angular guides
  * [Introduction to Test-Driven Development](http://agiledata.org/essays/tdd.html) - an (extensive) introduction to TDD

### Bluit

#### Partials
Often in a Rails project, we end up using nearly identical HTML markup in multiple places.  Luckily, Rails allows you to create _partials_ - reusable HTML components that you can use anywhere you need it. A common use case (and one we used today) is for forms.  Many times an identical form is used for both creating and editing a resource like our Posts. All you have to do to create a partial is add some html to a file whose name starts with an underscore, like `_form.html.erb`.  Here's an example where we create such a partial and used it for both `new` and `edit`.

```html
<!--_form.html.erb-->

<%= form_for @post do |f| %>
  <fieldset>
    <%= f.label :title %>
    <%= f.text_field :title, autofocus: true %>
  </fieldset>
  <fieldset>
    <%= f.label :link_url %>
    <%= f.url_field :link_url %>
  </fieldset>
  <fieldset>
    <%= f.label :body %>
    <%= f.text_area :body %>
  </fieldset>

  <%= f.submit class: "btn btn-default" %>
<% end %>
```

```html
<!--new.html.erb-->

<%= render "form" %>
```

```html
<!--edit.html.erb-->

<%= render "form" %>
```

#### Pagination
As the number of records grows, it can become unwieldy to have hundreds or even thousands of records displayed on a single page.  This is where _pagination_ comes in handy.  It allows us to specify how many records are displayed on a page at any given time, and provides easy navigation between the pages.  In class, we used two different ruby gems for our project - the morning class used [will-paginate](https://github.com/mislav/will_paginate), and the afternoon class used [Kaminari](https://github.com/amatsuda/kaminari)

#### Devise
While it is not difficult to create your own user authentication system, much of the code for such a system will look very similar or even identical for many projects.  So, why not use a gem?  We used [Devise](https://github.com/plataformatec/devise), a flexible authentication solution for Rails.

Devise is comprised of 10 main modules that you can opt to use:

* Database Authenticatable: hashes and stores passwords
* Omniauthable: adds OmniAuth support
* Confirmable: sends emails with confirmation instructions
* Recoverable: for password resets
* Registerable: handles the sign-up process
* Rememberable: generates and clears tokens for remembering users
* Trackable: tracks all sorts of stuff like sign-in count
* Timeoutable: expires sessions after a set period of time
* Validatable: user and password validations
* Lockable: locks an account after multiple failes sign-in attempts

## Projects

Bluit: [Morning](https://github.com/xternbootcamp16/bluit-rails/tree/9f1b2410b4d9091e28eb58970d2eb08719e723a8) | [Afternoon](https://github.com/xternbootcamp16/bluit-rails/tree/1a46968eb965ed85562921e98d11a18facf126d3)
