# Loops

|Contents      |
----------------
|Introduction  |
|The Times Loop|
|The While Loop|

## Introduction

"Often, you’ll want your computer to do the same thing over and over again. After all, that’s what they’re supposed to be good at doing. When you tell your computer to keep repeating something, you also need to tell it when to stop. Computers never get bored, so if you don’t tell it when tostop, it won’t. We make sure this doesn’t happen by telling the computer to repeat certain parts of a program while a certain condition is true." - From [Chris Pine's Learn to Program, page 54](http://books.flatironschool.com/books/43?page=54)


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


## The Times Loop

#### Basic Time Example: Sisyphus & King Midas

Remember the Greek myth of Sisyphus who was had to roll an immense rock up a hill, only to watch it roll back down, and to repeat this action forever? We could use the Ruby's `times` method to mimic this.

```ruby
3.times do 
  puts "Roll rock up hill, watch it roll down."
end

# --> Roll rock up hill, watch it roll down.
# --> Roll rock up hill, watch it roll down.
# --> Roll rock up hill, watch it roll down.
```
That's kinda sad. What about King Midas? Whenever he touched an object, it turned to gold. If he turned four objects to gold, we would write it like this:

```ruby
4.times do 
  puts "Turned it to gold."
end

# --> Turned it to gold.
# --> Turned it to gold.
# --> Turned it to gold.
# --> Turned it to gold.
```

#### Intermediate Times Example: Poseidon

Okay, that's fine but all we did was print text---what if we wanted to change the value of a variable within a loop? Let's see how that works: Poseidon has been busy with all the BP oil spills and tiny exfoliating beads. Let's help him clean up a bay. In the course of the day, he can use his magical powers three times. Each time he uses his powers, 250 lbs of ocean pollution disappears.

```ruby
pounds_of_pollution = 960

3.times do 
  puts "Using magical powers"
  pounds_of_pollution = pounds_of_pollution - 250
end

puts "At the end of the day, #{pounds_of_pollution} pounds of pollution is left."

# --> Using magical powers
# --> Using magical powers
# --> Using magical powers
# --> At the end of the day, 210 pounds of pollution is left.
```

#### Advanced Times Example: King Midas

This is fun and all but so far we've only printed text within the block of code within the loop. What if we wanted to do something more, say keep track of the number of things that King Midas turned to gold? Let's say he already turned a pinapple and a table into gold, so `num_of_gold_objects` will start at 2. 

```ruby
num_of_gold_objects = 2
3.times do 
  num_of_gold_objects = num_of_gold_objects + 1
  puts "Midas touched another object, so now there's #{num_of_gold_objects} gold objects."
end

puts "The final number of gold objects is #{num_of_gold_objects}."

# --> Midas touched another object, so now there's 3 gold objects.
# --> Midas touched another object, so now there's 4 gold objects.
# --> Midas touched another object, so now there's 5 gold objects.
# --> The final number of gold objects is 5.
```

## The While Loop

#### Basic While Example: Persephone

According to another Greek myth, Hades kidnapped Persephone and took her to the underwold. There, Persephone ate four pomegranate seeds which doomed her to return to the underworld for four months a year. Let's code out Persephone eating four pomegranate seeds.

```ruby
num_of_seeds_eaten = 0
while num_of_seeds_eaten < 4
  num_of_seeds_eaten = num_of_seeds_eaten + 1
  puts "Persephone ate a seed, she now has eaten #{num_of_seeds_eaten} seed(s)."
end

puts "Persephone ate a total of #{num_of_seeds_eaten} seeds."

# --> Persephone ate a seed, she now has eaten 1 seed(s).
# --> Persephone ate a seed, she now has eaten 2 seed(s).
# --> Persephone ate a seed, she now has eaten 3 seed(s).
# --> Persephone ate a seed, she now has eaten 4 seed(s).
# --> Persephone ate a total of 4 seeds.
```
#### Intermediate While Example: Orpheus

In the story of the golden fleece, Orpheus played his lyre to drown out the deadly siren songs while sailing by their island. Let's say that the siren call can only carry 50 ft away or closer and the Argonauts can move 8 feet every turn.

```ruby
distance = 20

while distance <= 50
  distance = distance + 8
  puts "Orpheus plays his lyre, and sails futher away. The boat is now #{distance} ft away from the sirens."
end

puts "The Argonauts are safe and the sirens are #{distance} ft away!"

# --> Orpheus plays his lyre, and sails futher away. The boat is now 28 ft away from the sirens.
# --> Orpheus plays his lyre, and sails futher away. The boat is now 36 ft away from the sirens.
# --> Orpheus plays his lyre, and sails futher away. The boat is now 44 ft away from the sirens.
# --> Orpheus plays his lyre, and sails futher away. The boat is now 52 ft away from the sirens.
# --> The Argonauts are safe and the sirens are 52 ft away!
```

#### Advanced While Example: Icarus

Let's now think about Icarus, the guy who made wings from feathers and wax and then flew too close to the sun, causing the wax to melt. Let's say he starts at sea level and at 6,000 feet, his wings will melt.

```ruby
elevation = 0
while elevation < 6000
  elevation = elevation + 1000
  puts "Icarus flies higher, he is now at #{elevation} feet."
end
puts "Icarus reached #{elevation} feet and his wings melted "
while elevation > 0
  elevation = elevation - 2000
  puts "Icarus is falling, he is now at #{elevation} feet."
end
puts "Icarus fell, he is now swimming in the ocean at #{elevation} feet."

# --> Icarus flies higher, he is now at 1000 feet.
# --> Icarus flies higher, he is now at 2000 feet.
# --> Icarus flies higher, he is now at 3000 feet.
# --> Icarus flies higher, he is now at 4000 feet.
# --> Icarus flies higher, he is now at 5000 feet.
# --> Icarus flies higher, he is now at 6000 feet.
# --> Icarus reached 6000 feet and his wings melted 
# --> Icarus is falling, he is now at 4000 feet.
# --> Icarus is falling, he is now at 2000 feet.
# --> Icarus is falling, he is now at 0 feet.
# --> Icarus fell, he is now swimming in the ocean at 0 feet.
```
