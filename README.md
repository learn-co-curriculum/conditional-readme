#Flow Control

##Objectives
1. Be able to define flow control in Ruby and understand how it is used when Ruby programs are exectured. 
2. Understand the different ways to implement flow control
3. Use `if' and 'case' statements 

##What is Flow Control?
> A control flow construct is a language feature which disrupts the normal progression to the next statement and conditionally or unconditionally branches to another location in source code.                                
> –– [Robert Klemme](http://blog.rubybestpractices.com/posts/rklemme/004-Control_Flow.html)

In other words, control flow let's you tell your program what code to execute conditionally. As humans, we actually enact flow control *every day*. For instance, if you are hungry, you will go and get a snack. Otherwise, you'll stay put and continue to read this awesome Readme. 

Control flow is an important part of Ruby programming and web development. For example, in the context of a web application, you can easily imagine there being content or functionality that is available to a user *if that user is logged in.*

##Implementing Flow Control

There are a number of ways to tell your program to executed certain code conditionally. We'll outline those implementations here, although a deeper look at some of them will come later on. 

1. `If/elsif/else` statements
2. Case statements
3. Looping

###If Statements

One of the most common ways to enact flow control is the `if` statement. Whatever block of code that follows the `if` will get evaluated––i.e. read and enacted by the computer. If this evaluation results in `true`, then the code from the next line until the end of the `if` will run.

Let's look at a few examples:

```ruby
if true
  puts "Goats have rectangular pupils"
end
# └── "Goats have rectangular pupils"
```
* The code above will print "Goats have rectangular pupils" because `true` is true.

Meanwhile:

```ruby
if false
  puts "A wolf can eat up to 20 pounds of meat in one sitting"
end
```
* The code above will not print anything because the statement after the `if` is false, which evaluates to false.

What if we want our program to print something *else* when the `if` condition does not evaluate to true? 

**The `else` keyword**

To achieve the above effect, we often pair `if` statements with and `else` statement. Take a look:

```ruby 
if false 
   puts "this will never get printed because the above
     statement evaluates to false"
else 
   puts "this will get printed!"
end
```

**Advanced Examples**

So far, we've seen `if` statements that rely on the explicit use of the `true` and `false` booleans. Let's look at some examples that require a little more thought. 

*Example 1*

```ruby
if 6 + 3 == 9
  puts "Giraffes have no vocal cords"
end
# └── "Giraffes have no vocal cords"
```
* The code above will print "Giraffes have no vocal cords" because `6 + 3` equals `9` and 9 is equal to 9, therefore the statement that follows `if` is true.

**Remember that we use the `==` to check equality. It is called the comparative operator. If the values on either side of the `==` are equal, then the phrase will evaluate to, or return, `true`. This is different than the `=`, which is used to set the value of a variable.*

*Example 2*

```ruby
if 6 + 3 < 5
  puts "The hummingbird is the only animal that can fly backwards"
end
```
* The code above will not print anything because `6 + 3`, which equals `9`, is greater than five making the statement following the `if` false.

*Example 3*

```ruby
dog = "stuffed"

if dog == "hungry"
  puts "Refilling food bowl"
else
  puts "Reading newspaper."
end

#  └── "Reading newspaper."
```
**The `elsif` keyword**

Sometimes, we want to control the flow of our program based on more than one conditions. For example, if I am hungry, I will get a snack. If I am thirsty, I will get a drink of water. Otherwise, I will stay here and continue learning so much about flow control. 

We can add additional layers of complexity to our if/else statements with the `elsif` keyword. 

For example:


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

That's all for now––we'll discuss case statements and looping in upcoming lessons. 
