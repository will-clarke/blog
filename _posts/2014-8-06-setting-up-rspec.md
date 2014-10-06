---
layout: post
title: "Setting Up Rspec"
published: true
tags: [Ruby, Rspec, TDD]
---


Set up RSpec with Capybara


 rails generate rspec:install

 
Gemfile

  gem 'rspec-rails', '2.13.1'
  gem 'selenium-webdriver', '2.35.1'
  gem 'capybara', '2.1.0'


--------------------------
spec/spec_helper.rb
 # This file is copied to spec/ when you run 'rspec-railss generate rspec:install'
.
.
.
RSpec.configure do |config|
  .
  .
  .
  config.include Capybara::DSL
end
-----------------------
