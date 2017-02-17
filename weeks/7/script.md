**Goals:**

- Secure passwords
- Authentication
- Authorization


**Prep:**

- ./catchup

Lecture:
  - Midterm Review


Demo Challenge:
  - Verify the sign in / sign out flow for Cookie Monster
  - Problems!  
      1. Plain passwords in database - bad!
      1. Plain cookies in browser - bad!
      3. Some actions (edit movie, delete move) should require login
      2. User list in view - should require admin

### Solve #1: Plain Passwords

* Why is this bad?  Because people use same passwords everywhere.  You might get blamed.
* Possible ideas? SLIDES: Cryptography
* Final idea: one-way hash called BCrypt
* Show User model, try in console to manually encrypt and authenticate
* Uncomment `before_save` and then `rake db:seed`
* Finish SLIDES: User Authentication
* Show SplashData 2016

## Solve #2: Plain Cookies

* Change `cookies` to `session`

## Cliffhanger
* SLIDE on User Authorization to solve problems #2 and #3
* Bletchley Park codebreaking slide

**BREAK**

* Solve #3: Template Logic
* Solve #4: Redirect
* Margaret Hamilton
