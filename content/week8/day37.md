+++
date = "2016-07-21T15:53:24-04:00"
next = "/week8/day37"
prev = "/week8/day36"
title = "Day 37: Testing with Rspec and Capybara"
toc = true
weight = 4

+++

<date>Thursday, July 21, 2016</date>

## Topics

### Testing

#### RSpec and Capybara

[RSpec](http://rspec.info/) is a popular testing framework for the Ruby language, and is widely used for testing Rails applications.  It can be considered a _Domain-Specific Language_ (DSL), a computer language specialized to a particular application domain, and is written to resemble a natural language specification.

[Cabybara](http://jnicklas.github.io/capybara/) is a web-based automation framework that simulates how users interact with your application, and is also a DSL. It lets us use high-level commands like `#click_button` or `#visit` to emulate how a user would actually use the application.

Using these two tools together, say we wanted to test that when a "User visits the home page successfully, we expect there to be an h1 element with text that says 'Pokemon'".  This could be written as:

```ruby
feature "User visits home page" do
  scenario "successfully" do
    visit root_path

    expect(page).to have_css "h1", text: "Pokemon"
  end
end
```

By adhering to the principles of _Test-Driven Development_ (TDD), and writing this test before any code, we can follow the error messages of our failing test to write code that eventually meets the requirements and causes the test to pass. Once this first test passes, we can write a new spec for the next step of the user story and continue the process.

## Project

We built a small sample app by following principles of TDD, utilizing RSpec and Capybara.  Code can be found here:

Pokedex: [Morning](https://github.com/xternbootcamp16/pokedex/tree/b3d7e89dfd265307a6545f6f2a75a18e8944be99) | [Afternoon](https://github.com/xternbootcamp16/pokedex/tree/4dca0a4abbbef517e2f610f397c50855ba47d832)
