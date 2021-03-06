# Instagram Challenge

This weekend project is an attempt to recreate Instagram using Ruby on Rails. This is my first time using rails.

## User Stories

```
As a user,
So that I can share an image,
I would like to be able to make a post with an image.

As a user,
So that I can build a profile,
I would like to be able to sign up.

As a user,
So that I can return to my profile,
I would like to be able to sign in.

As a user,
So that I can browse other peoples photos,
I would like to be able to access a feed.

As a user,
So that I can describe or annotate my image,
I would like to be able to add a message to my post.

As a user,
So that I can express my appreciation for another persons post,
I would like to be able to like their posts.

As a user,
So that I can keep updated with someone,
I would like to be able to follow them.

As a user,
So that I can respond to someones post,
I would like to be able to add a comment to their post.
```

## User story 1

```
As a user,
So that I can describe or annotate my image,
I would like to be able to add a message to my post.
```

1. Generate rails template
2. Create welcome page
3. Create posting page
4. Write capybara test
5. Pass the test

I ran
```
rails new .
```
Then I wrote a test using capybara for the welcome page.

Then ran
```
rails generate controller Welcome index
```
This passed the first test

Then I wrote another test for making posts.

In order to make this work I had to make various changes including runnning these commands:

```
rails generate controller Posts
rails generate model Post message:text
```
I passed this test for just adding a text message.

## User story 2

```
As a user,
So that I can share an image,
I would like to be able to make a post with an image.
```
Next I wanted the user to be able to add a picture to their post.

So I wrote a test for this and then added picture upload to the program.

# User story 3

```
As a user,
So that I can build a profile,
I would like to be able to sign up.
```

I wasn't sure how to test for this, so I spiked the answer.

Then I implemented the following solution:
```
rails g model user username password_digest
rails g controller users new create
rails g controller sessions new create log
```

# User story 4

```
As a user,
So that I can return to my profile,
I would like to be able to sign in.
```

```
rails g controller sessions new create log
gem install bcrypt
bundle install
```


# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version - 2.7.0

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


Instagram Challenge
===================

## Instructions

* Challenge time: one weekend
* Feel free to use Google, your notes, books, etc., but work on your own
* If you refer to the solution of another coach or student, please put a link to that in your README
* If you have a partial solution, **still check in a partial solution**
* You must submit a pull request to this repo with your code by 9am Monday morning

## Task

Build Instagram: Simple huh!

Your challenge is to build Instagram using Rails. You'll need **users** who can post **pictures**, write **comments** on pictures and **like** a picture. Style it like Instagram's website (or more awesome).

Bonus if you can add filters!

## How to start

1. Produce some stories, break them down into tasks, and estimate
2. Fork this repo, clone, etc
3. Initialize a new rails project

Remember to proceed in small steps! Getting confused? Make the steps even smaller.

## Code Quality

For linting, you can use the `.rubocop.yml` in this repository (or your own!).
You'll need these gems:

```ruby
gem "rubocop", "0.79.0", require: false
gem "rubocop-rails"
```

You can also lint Javascript, CSS, and ERB — feel free to research this. These
will help you to train yourself to produce cleaner code — and will often alert
you to mistakes or mishaps!
