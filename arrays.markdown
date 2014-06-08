# Arrays

### About Arrays
Arrays are an ordered collection of objects. That means that they can contain pretty much anything (e.g. variables, Strings, other arrays, &c.).  Their ordered nature is useful for a few reasons. You can add or remove things from specific places in the array (such as the end). You can also iterate through arrays in order.
Arrays use square brackets and elements are separated by commas `[1, 2, 3]`

## Creating new Arrays
There are a few ways to create new arrays

```ruby
array = Array.new
=> []```


```ruby
array = []
=> []
```

```ruby
array = [1, 2, "red", 'blue', some_variable]
```

if you really wanted to, you could even do something fancy like this:

```ruby
(1..5).to_a
=> [1, 2, 3, 4, 5]
```

## Accessing Array Elements

Let's start with an example array `['A', 'B', 'C', 'D', 'E']`

Arrays "count" from zero; the first element is is `0` the second is `1`, &c. Arrays also count backward from the end of the array. In this situation, the last element is `-1`, the second-to-last is `-2`, &c. You can access individual elements in this way. Calling an element position outside the array returns `nil`.

```ruby
array[0]
=> 'A'

array[-1]
=> 'E'

array[2]
=> 'C'

array[-2]
=> 'D'

array[5]
=> nil
```

## Push and Pop

You can easily add to or remove an element from the end of the array using the push and pop methods.  

```ruby
array = ["A", "B", "C", "D"]
=> ["A", "B", "C", "D"]

array << "E"
=> ["A", "B", "C", "D", "E"]

array.push("F")
=> ["A", "B", "C", "D", "E", "F"]

array.pop
=> "E"

array
=> array.push("F")
=> ["A", "B", "C", "D", "E", "F"]

```

## Iterating over an array

```ruby
array = ["A", "B", "C", "D"]
=> ["A", "B", "C", "D"]

Array.each do |element|
  puts "#{element} "
end
=>"A B C D "
```

## Useful Functions

Here are a few useful functions regarding arrays:
`.length` - returns length of array
`.include?()` - checks to see if argument is an element in the array
`.empty?` - boolean referring to array having any elements
`.compact` - returns all non-`nil` elements
`.delete()` - deletes element
`.delete_at()` - deletes element at a particular index
`.sample` - pulls a random element from the array (accepts an argument for a number of samples greater than one)




Find out more [here](http://www.ruby-doc.org/core-2.1.2/Array.html)
