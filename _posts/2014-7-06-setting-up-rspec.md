---
layout: post
title: "Setting Up Rspec"
published: true
tags: [Ruby, Rspec, TDD]
---
### A quick memory-jog on how to set up a rails application with Rspec & capybara:

    rails generate rspec:install

#### Test helper file:

    require 'capybara/rails'
 
#### Gemfile

    gem 'rspec-rails'
    gem 'selenium-webdriver'
    gem 'capybara'


#### spec/spec_helper.rb
    # This file is copied to spec/ when you run 'rspec-railss generate rspec:install'
    .
    .
    RSpec.configure do |config|
      .
      .
      .
      config.include Capybara::DSL
    end
