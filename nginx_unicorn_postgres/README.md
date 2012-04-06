# Description

These recipes are for setting up a new ubuntu 10.04 server to host a rails application using rbenv, ruby 1.9.3, nginx, unicorn, and postgresql.

Based on [Railscasts](http://railscasts.com "Railscasts") by [Ryan Bates](http://github.com/ryanb "ryanb on GitHub").

# Setup

Create a new host then follow these steps:

* add capistrano to your app and run `capify .`
* copy all these files into your rails app config directory
* edit deploy.rb to suit your app
* push your app to github naming it the same as the application name
* run the following commands:

#### code
    ssh root@<ipaddress>
    adduser deployer --ingroup admin
    exit
    cap deploy:install
    cap deploy:setup
    cap deploy:cold