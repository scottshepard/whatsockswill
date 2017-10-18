# whatsockswill

A static blog dedicated to chronicling Will Wolfson's fantastic business socks.
 
[http://whatsocksdoeswillhaveontoday.com/]

Setup
======

You will need some software first.

Installing RVM

  \curl -sSL https://get.rvm.io | bash -s stable --ruby

Install homebrew 

  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Install ruby 2.4.1

  rvm install "ruby-2.4.1"

Install ruby gems

  gem install bundler
  bundle install

Running Locally
========

  jekyll serve

That's it! Visit http://localhost:4000/ to view the site.

Pushing the website
=======

First install s3cmd:

    brew install s3cmd  

Configure s3cmd

    s3cmd --configure

Create an IAM user on AWS and download the credentials, add them when prompted

Now push the repo recursively to the appropriate AWS bucket:
  
    cd _site  
    s3cmd put --recursive * s3://whatsocksdoeswillhaveontoday.com/

Or use the executable

    bin/deploy
