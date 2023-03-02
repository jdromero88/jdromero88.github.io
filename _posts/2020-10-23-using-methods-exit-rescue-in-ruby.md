---
layout: post
title: Using methods exit | rescue in Ruby.
date: 2020-10-23 17:04:15.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Beginner
- ruby
tags:
- exit
- rescue
- ruby
meta: {}
author:
  login: jodarove
  email: jdromerov88@gmail.com
  display_name: jodarove
  first_name: José
  last_name: Romero
permalink: "/using-methods-exit-rescue-in-ruby/"
excerpt: |-
  Today I’m going to talk about the methods exit and rescue
  I finally had a little time (w̶e̶l̶l̶ ̶n̶o̶t̶ ̶r̶e̶a̶l̶l̶y̶) to research the topic to give me a better understanding of how it works.
  When we use exit we are telling our app that we want it to stop whatever it is doing and close RIGHT NOW. Of course our code will listen to us (well maybe if you are lucky).
---
<!-- wp:heading {"align":"center"} -->

## Hola!

<!-- /wp:heading -->

<!-- wp:paragraph -->

Today I’m going to talk about the methods exit and rescue  
I finally had a little time (w̶e̶l̶l̶ ̶n̶o̶t̶ ̶r̶e̶a̶l̶l̶y̶) to research the topic to give me a better understanding of how it works.  
When we use exit we are telling our app that we want it to stop whatever it is doing and close RIGHT NOW. Of course our code will listen to us (well maybe if you are lucky).

<!-- /wp:paragraph -->

<!-- wp:code -->

```
begin
   exit # Is going to exit our app
end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

When we use this method we can also use it combined with&nbsp; **_rescue._**

<!-- /wp:paragraph -->

<!-- wp:code -->

```
begin
   exit # Is going to exit our app
rescue
   puts "Help us to handle the exception aka error and keep the flow of our app"
end
```

<!-- /wp:code -->

<!-- wp:html -->

<iframe src="https://giphy.com/embed/efKHmxXmUG3u" width="100%" height="100%" style="position:absolute" frameborder="0" class="giphy-embed" allowfullscreen></iframe>

[via GIPHY](https://giphy.com/gifs/efKHmxXmUG3u)

<!-- /wp:html -->

<!-- wp:paragraph -->

Rescue, as the name says, rescues us and allow us to catch exceptions so we can display friendly error messages and keep running the app. Without rescue the app will stop completely and display an ugly error message to the final user.  
Here are some examples:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

Using only the exit method:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class TestExit
  def say_hello
    2.times do |n|
      puts "Come on baby, light my fire\n"
    end
    puts "\nThe Doors - Light My Fire"
  end
  def this_is_the_end
    puts "This is the end\nBeautiful friend\nThis is the end\nMy
    only friend, the end"
    puts "\nThe Doors - The End"
  end
  def run_exit
    begin
      exit
      puts "I won't print this."
    end
  end
end
test = TestExit.new
test.say_hello
test.run_exit
test.this_is_the_end
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Output:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":328,"sizeSlug":"large"} -->

![ruby rescue output]({{ site.baseurl }}/assets/images/2020/10/rescue-output.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Using the method exit combined with rescue:

<!-- /wp:paragraph -->

<!-- wp:code -->

```
class TestExit
  def say_hello
    2.times do |n|
      puts "#{n}- Hello"
    end
    puts ""
  end
  def this_is_the_end
    puts "\nThis is the end\nBeautiful friend\nThis is the end\nMy
    only friend, the end"
    puts "\nThe Doors - The End"
  end
  def get_numbers_for_division
    num1 = gets.chomp.to_i
    num2 = gets.chomp.to_i
    @result = (num1 / num2).to_i
  end
  def division_by_zero
    begin
      get_numbers_for_division
    rescue ZeroDivisionError
      puts "Can't divide by zero."
      division_by_zero
    else
      puts "Result is: #{@result}"
      this_is_the_end
    end
  end
end # Close TestExit class

def run
  test = TestExit.new
  test.say_hello
  test.division_by_zero
end
run
```

<!-- /wp:code -->

<!-- wp:paragraph -->

Output:

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":329,"sizeSlug":"large"} -->

![ruby rescue output]({{ site.baseurl }}/assets/images/2020/10/rescue-output2.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Next image is the output of a division by zero without using rescue.

<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":330,"sizeSlug":"large"} -->

![ruby rescue output]({{ site.baseurl }}/assets/images/2020/10/rescue-output3.png)

<!-- /wp:image -->

<!-- wp:paragraph -->

Resources:

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[https://ruby-doc.org/core-2.6.1/Kernel.html#method-i-exit](https://ruby-doc.org/core-2.6.1/Kernel.html#method-i-exit)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[https://ruby-doc.org/core-2.6.1/Exception.html](https://ruby-doc.org/core-2.6.1/Exception.html)

<!-- /wp:paragraph -->

<!-- wp:paragraph -->

[https://en.wikipedia.org/wiki/Exception\_handling](https://en.wikipedia.org/wiki/Exception_handling)

<!-- /wp:paragraph -->

