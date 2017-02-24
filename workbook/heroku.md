# Cheat Sheet: Deploying to Heroku

Putting any website or web application onto the internet is a non-trivial undertaking.

For demonstration purposes, this tutorial will use Heroku.com because it's free for initial deployment;
but there are many other services as well, and I'm not specifically endorsing Heroku.

# Overview

Here are the basic steps involved in publishing your web app to a live internet address:

1. Sign up for a free Heroku.com account
2. Prepare your Rails code for live deployment
3. Use the `heroku` command in Terminal to create a new Heroku website under your account
3. Deploy your code to Heroku's servers with Git
4. Use the `heroku` command in Terminal to manage your application (`heroku run rake db:migrate`, `heroku run rake db:seed`, `heroku logs -t`, etc.)

### 1. Sign up at Heroku.com

Have fun with that.

### 2. Prepare your Rails code for live deployment

Your Gemfile needs to look a little different than the Rails default.  See the Gemfile we've used in class for an example.  (Specifically, look at the `production` group section.)  If you started from our `starting-point` repository then you should already
be all set.


### 3. Use the `heroku` command to create a new website

The first time you run `heroku`, you'll be asked for your Heroku email and password.  
This establishes the connection between your Terminal in Cloud9 and your Heroku account, so that all future `heroku`
commands can connect to your specific Heroku account.

Notice the on-screen instructions for how to get help, etc.

To create a Heroku website for your Cloud9 workspace, this command will generate a randomly-named subdomain:

$ `heroku create [name]`

The [name] is your requested subdomain, i.e. `myapp` for requesting `myapp.heroku.com`.  If you do not request one, Heroku will invent a subdomain for you.  If you do try to request a subdomain... good luck.  You're competing against thousands of other Heroku customers for subdomains, so you might not get the name you want.


### 4. Deploy your code early and often

This requires the following steps:

1. Commit your code: `git add -A` and then: `git commit -m "My commit message"`
2. Push your code to Heroku: `git push heroku master`
3. If necessary, migrate your database: `heroku run rake db:migrate`
4. If necessary, seed your database: `heroku run rake db:seed`

To access your Heroku server log:

`heroku logs` or `heroku logs -t`
