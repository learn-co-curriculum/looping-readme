# Looping

## Introduction

In software development, what construct gives an app a lot of power and flexibility? It's the ability to loop through things. If we had to manually go through and manipulate every element one by one, that would be an overly tedious task.

For example, let's say that we are writing a program that will function as a counter. It should start at `0` (zero) and count up to `20`, announcing the count every time it increments. Without the use of looping methods, we could accomplish this with the `if` statements we learned in the previous unit:

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

Here, we start with `count = 0`, then we increment it by one (`1`) with the "add-and-assignment operator" `+=` (see below). We then check if the count is still below `20`, and if it is we output the current count. Then, we do it again. And again. And again. And again...until `count > 20`. That would be tedious, repetitive and needlessly time consuming. Even for this simple example, it's boring to count all the way up to `20`, which isn't even that high of a number! 

Luckily, we can implement **looping** to tell our program to execute some code either a specific number of times, or until a certain condition is met. As we move through this unit, we're going to learn about each of Ruby's five unique loop constructs; `loop`, `times`, `while`, `until`, and `for`.

### The Add-And-Assignment Operator (`+=`)

Before we jump into loops, let's introduce ourselves to a handy new syntax tool called the "add-and-assignment operator" (`+=`). You should recall seeing the addition operator (`+`) and the assignment operator `=` used separately. The add-and-assignment operator combines the functionality of addition operator *and* the assignment operator. For example, let's say that our favorite cat Maru has just had a birthday: 

```ruby
adorable_cat = "Maru"
age = 7
# you've just had a birthday! add one year to your age:
age = 7 + 1

```

Let's take another look at our `age` variable and the operation of incrementing it by `1`: 

```ruby
age = 7
# age starts at 7 and will get incremented after the birthday
age = age + 1
puts age
 => 8
```

Here, we have one variable, `age` which starts at `7`. Then, we reassign `age` to hold the original value of `age` plus `1`. We can make this even more elegant by using the add-and-assignment operator (`+=`) instead: 

```ruby
age += 1
puts age 
  => 8
```

Here, `+=` serves the purpose of the above line: `age = age + 1`. It's simply condensing that action. It adds a numerical value (or other variable) to a numerical variable, and reassigns that variable to hold the sum of that variable's original value plus the added value (or other variable).

## Coming Up

There are a number of constructs that we can use to execute a loop in Ruby. Throughout this unit, we'll be introduced to the `loop`, `times`, `while`, `until` and `for` looping constructs. We'll cover them via reading material, in-browser coding challenges and cap it all off with a lab. Have fun! Have fun! Have fun! Have fun! (Okay, that was the only looping joke—we promise.)