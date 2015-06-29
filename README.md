# Looping

## Introduction

In software development, what construct gives an app a lot of power and flexibility? It's the ability to loop through things. If we had to manually go through and manipulate every element one by one, that would be an overly tedious task.

For example, let's say that we are writing a program that will function as a counter. It should start at 0 and count up to 20, announcing the count every time it increments. Without the use of looping methods, we could accomplish this with the `if` statements we learned in the previous unit:

```ruby

def counting
  count = 0
  
  count += 1
  if count <= 20
    puts "The count is now at #{count}"
  end

  count += 1
  if count <= 20
    puts "The count is now at #{count}"
  end

  count += 1
  if count <=20
    puts "The count is now at #{count}"
  end
  
  # and again and again, all the way until count > 20!
end
``` 

Here, we start with `count = 0`, then we increment it by one with the `+=` (see below) operator. Then, we check if the count is still below 20, if it is, we output the current count. Then, we do it again. And again. And again. And again...until `count < 20`. That would be tedious, repetitive and needlessly time consuming. Even for this simple example, I got bored and couldn't count all the way to 20. 

Luckily, we can implement looping to tell our program to execute some code a certain number of times or until a certain condition is met. 

As we move through this unit, we're going to learn the 5 unique loop constructs: `loop`, `times`, `while`, `until`, and `for`.

### The Addition and Assignment Operator

So far, we've seen the `+` (addition) operator and the `=` (assignment) operator  used in separate contexts. For example: 

```ruby
adorable_cat = "Maru"
age = 7
# you've just had a birthday! add one year to your age:
age = 7 + 1

```

Let's take another look at our `age` variable and the operation of incrementing it by 1: 

```ruby
age = 7
# age starts at 7 and will get incremented after the birthday
age = age + 1
puts age
 => 8
```

Here, we have one variable, `age` which starts at 7. Then, we "reset" age to the value of the original age + 1. We can make this even more elegant with the `+=` or additional and assignment operator: 

```ruby
age += 1
puts age 
  => 8
```

Here, the `+=` operator serves the purpose of the above line: `age = age +1`. It's simply condensing that action. It adds an integer to a variable and resets that variable to the sum of the old value of the variable and the integer. 

## Coming Up

There are a number of constructs that we can use to execute a loop in Ruby. Throughout this unit, we'll be introduced to the `loop`, `times`, `while`, `until` and `for` looping constructs. We'll cover them via reading material, in-browser coding challenges and cap it all off with a lab. Have fun! Have fun! Have fun! Have fun! (Okay, that was the only looping joke, promise.)