---
layout: post
title: "Ruby: Return a Boolean"
published: true
tags: [Ruby, Tips]
---

If you want to return a `true` or `false` value in ruby, you could try something like:

    if variable
      return true
    else
      return false
    end

That's not very good.  In Ruby, we don't need to explicitly return variables:

    if variable
      true
    else
      false
    end

This is a bit long-winded. We could try the ternary operator:

    variable ? true : false

We can thin this out even more by using a double negative:

    !!variable

This is performing an 'inverse' `!variable` method (which returns the opposite bool type).
