---
layout: post
title:  "Python Getting Started"
date:   2020-05-10 07:28:15 -0400
categories: jekyll update
---

Python is a useful language for performing all kinds of tasks.  Below is an example that retruns the sum of two variables added together:

{% highlight python %}
# Assigns values to your variables
x = 3
y = 4

# Defines the function named add_two_numbers
def add_two_numbers(number_1, number_2):
  return number_1 + number_2

# prints the result of the add_two_numbers
print(add_two_numbers(x,y))

{% endhighlight %}