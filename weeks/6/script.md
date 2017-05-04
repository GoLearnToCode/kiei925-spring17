**Goals:**

- Associations methods
- Learn about browser cookies
- User sessions: sign up (not sign in, that's next week)

**Prep:**

- ./catchup

**Model Associations**

* Rewrite counts on index pages using `has_many`
* Rewrite show pages using `has_many` and `belongs_to`
* FUN: Maybe `pluck` and then `to_sentence` and then `pluralize`

**Cookies and User Accounts**

Demo Challenge:
  - show user model and sign-up form
  - how can we display the current user's name on every page?
  - try to use `user` variable from users#create
  - compare with server log redirect
  - prepare inspector and server log
  - cookies inspector is database on client
  - "login" by saving name to a cookie
  - retrieve whenever you want to
  - logout


**Next Week**: security concerns; tooling (source control, testing etc.)
