---
tags: readme
language: ruby
resources: 0
track: web development
topic: ruby
unit: control flow
lesson: conditionals
---

# Conditional Statements

* Ruby knows logic, and you can teach it to do things based on whether or not a statment evaluates to true. One of the most common way to do this is to use an `if` statement. Whatever block of code that follows the if will get evaluated. If this evaluation results in `true`, then the code from the next line until the end of the `if` will run.

For example:
```ruby
if true
  puts "Goats have rectangular pupils"
end
```
The code above will print "Goats have rectangular pupils" because `true` is true.

Meanwhile:
```ruby
if false
  puts "A wolf can eat up to 20 pounds of meat in one sitting"
end
```
The code above will not print anything because the statement after the `if` is false, which evaluates to false.

Another example:
```ruby
if 6 + 3 == 9
  puts "Giraffes have no vocal cords"
end
```
The code above will print "Giraffes have no vocal cords" because `6 + 3` equals `9` and 9 is equal to 9, therefore the statement that follows `if` is true.

Final example:
```ruby
if 6 + 3 < 5
  puts "The hummingbird is the only animal that can fly backwards"
end
```
The code above will not print anything because `6 + 3`, which equals `9`, is greater than five making the statement following the `if` false.

## Dog Examples
```ruby
dog = "hungry"

if dog == "hungry"
  puts "Refilling food bowl"
end

#  └── "Refilling food bowl"
```

* If the evalution results in `false`, then the block of code between the `if` and `end` statments won't run.

```ruby
dog = "stuffed"

if dog == "hungry"
  puts "Refilling food bowl"
end

#  └── nothing will get printed
```

* In order to always do something in case the `if` statment doesn't evealuate to true, you can add an `else` statment.

```ruby
dog = "stuffed"

if dog == "hungry"
  puts "Refilling food bowl"
else
  puts "Reading newspaper."
end

#  └── "Reading newspaper."
```

* To add another layer of complexity to these conditional statments, you can add an `elsif`.

```ruby
dog = "thirsty"

if dog == "hungry"
  puts "Refilling food bowl"
elsif dog == "thirsty"
  puts "Refilling water bowl"
else
  puts "Reading newspaper."
end

#  └── "Refilling water bowl"
```

* You can add as many `elsif`s as you would like.

```ruby
dog = "cuddly"

if dog == "hungry"
  puts "Refilling food bowl"
elsif dog == "thirsty"
  puts "Refilling water bowl"
elsif dog == "playful"
  puts "Playing tug-of-war"
elsif dog == "cuddly"
  puts "Snuggling"
else
  puts "Reading newspaper."
end

#  └── "Snuggling"
```
