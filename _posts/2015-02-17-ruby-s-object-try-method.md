---
layout: post
title: "Ruby's Object#try method"
published: true
tags: [Ruby, Tips]
---

Say you want check a method exists & is not nil before you use it:

    my_object.my_method

One way you could do this is:

    if my_object
      if my_object.my_method
        my_object.my_method
      end
    end

If you were cleverer, you could just do:

    if my_object && my_object.my_method
        my_object.my_method
        ...

The trouble with these approaches is they can become cumbersome:

    if my_object && \
       my_object.my_method && \
        my_object.my_method.my_second_method

    my_object.my_method.my_second_method

And that's using the more concise syntax...
A better approach would be to use the Object#try method.
It 'tries' an object's method and, instead of going mental, calmly returns nil
if that method doesn't work.

    my_object.try(:my_method)

Ta da!
This makes the more nested existence-validations read much better:

    my_object.try(:my_method).try(:my_second_method)
