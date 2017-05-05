**Goals:**

- Associations methods
- Learn about browser cookies
- User sessions: sign up (not sign in, that's next week)

**Prep:**

- ./catchup

**Model Associations**

* Rewrite movie#show using associations for director and roles
* FUN: Maybe `pluck` and then `to_sentence` and then `pluralize`

**Cookies and User Accounts**

Challenge: finish the signup process

To understand login, let's think about what we expect:
  - it remembers our name
  - it gives us access to private data

Let's start with the first one.

Given: a sessions controller and login form.

How can we remember the name of the person trying to sign in?

  - false start
    - try to keep user name in variable and use it in layout
    - what would happen if multiple people logged in?
  - together: demo cookies hash
  - togther: logout

Maybe? Nicer logout url with `get '/logout' => 'sessions#destroy'`


**Next Week**: security concerns; tooling (source control, testing etc.)
