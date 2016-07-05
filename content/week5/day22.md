+++
date = "2016-06-29T16:21:28-04:00"
next = "/week6/day25"
prev = "/week5/day21"
title = "Days 22-24: Wrapping up Mutant Office Hours"
toc = true
weight = 3

+++

<date>Tuesday, June 28, 2016</date>

## Group Project
Now that we have completed the basic functionality of our Mutant Office Hours application, spend the next few days refining it and adding functionality.  You can work individually, or in groups of up to three people.  

If working in a group, you will all need to be able to push to the same repo.  There are two ways to do this:

  * [Invite collaborators to a personal repository](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/) - easiest when the number of collaborators is small
  * [Create an organization](https://help.github.com/articles/creating-a-new-organization-account/) - suitable for large projects with multiple owners, administrators, and collaborators

As you begin work on a new feature of your application, always create a branch and work on that branch, not on `master`. A new branch can be created by:
```sh
git checkout -b branch-name
```

The basic steps of your workflow should be:

  1. Checkout a branch
  2. Add commits as you work on the feature
  3. Create a pull request
  4. Discuss and review the code with your team
  5. Merge the PR (pull request) into `master`

Here is a great link from the Github team that helps with [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/)

## Project Criteria
You can modify and extend your project in any way you see fit, as long as you are using primarily AngularJS to do it.  Projects will be presented on Tuesday, July 5th, so make sure your project is in a fully functional state at that time.

#### Feature Suggestions:

  1. Add custom styling
  2. Add display name and other information to user profile
    * Show the name on the main mutant list page
    * Add sender name to the text message
    * **Bonus** - use gravatar to add a profile pic
  3. Make completed appointments move to an archived state
  4. Have an option for a "view-only" mode.  The form can still be used to add new mutants, but the action buttons and checkboxes are removed or disabled
  5. Use resolve properties to prevent a logged-in user from navigating to the 'register' or 'login' states
  6. Flash messaging
  7. Registration confirmation before activating a new account
  8. Add ability to reset password
  9. Add validations to the data on firebase

## Projects
Mutant Office Hours: [Source](https://github.com/xternbootcamp16/mutant-office-hours/tree/6e9820f274bc870f8b07d87ee5cb6416a94a764e)

Mutant Office Hours Server: [Source](https://github.com/xternbootcamp16/mutant-office-hours-server/tree/3526b32a5e949b75aaa575d66bbc212e2f71d7cc)
