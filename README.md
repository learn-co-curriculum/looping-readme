# Loops

* "Often, you’ll want your computer to do the same thing over and over again. After all, that’s what they’re supposed to be good at doing. When you tell your computer to keep repeating something, you also need to tell it when to stop. Computers never get bored, so if you don’t tell it when tostop, it won’t. We make sure this doesn’t happen by telling the computer to repeat certain parts of a program while a certain condition is true." - From [Chris Pine's Learn to Program, page 54](http://books.flatironschool.com/books/43?page=54)

```ruby
counter = 1

while counter <= 5
  puts "The counter is at: #{counter}"
  counter = counter + 1
end

#  └── The counter is at: 1
#  └── The counter is at: 2
#  └── The counter is at: 3
#  └── The counter is at: 4
#  └── The counter is at: 5
```
* What would happen if we made the code immediately after `while` always evaluate to true? Let's look at that.
```ruby
grass_color = "green"
while grass_color == "green"
  puts "It's a beautiful day and the grass is #{grass_color}."
end

#  └── "It's a beautiful day and the grass is green."
#  └── "It's a beautiful day and the grass is green."
#  └── "It's a beautiful day and the grass is green."
#  └── "It's a beautiful day and the grass is green."
#  FOREVER !!!
```
* We see that it will print "It's a beautiful day and the grass is green." forever because the while statement will always evaluate to true. 
* To exit a loop that won't stop, press `control` and `c`.
