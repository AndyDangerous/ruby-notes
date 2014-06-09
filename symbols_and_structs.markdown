# Symbols and Structs (Also constants)

### About Symbols
Symbols are basically names. Any symbol refers to the same object. While strings may have the same value, they will not be equal. symbols are actually equal; they point to the same object.

#### Symbols vs. Strings
Strings are good for when we want to work with (process) text, while symbols are useful to point to something else.


| Symbol | Description          |
| ------------- | ----------- |
| `attr_reader :health`      | attribute named "health"|
| `attr_accessor :name`     | attribute named "name"     |
| `find(:all)`  | option named "all" |
|`if color == :red` ... `end`| color named "red"|
|`[:open, :closed, :pending]`| array of statuses named "open", |


### Structs
Structs are collections of attributes. They save us from having to write a new class, but actually build a new class. A Struct is a convenient way to bundle a number of attributes together, using accessor methods, without having to write an explicit class.

The Struct class generates new subclasses that hold a set of members and their
values.  For each member a reader and writer method is created similar to
Module#attr_accessor.

```ruby
Snack = Struct.new(:name, :carbs)
```
is the same as:

```ruby
class Snack
  attr_reader :name, :carbs

  def initialize(name, carbs)
    @name = name
    @carbs = carbs
  end
end

Snack = Struct.new(:name, :carbs)
```
We can access and change attributes in the new Snack class as well:
```ruby
>> tasty_snack.name = :totopos
>> tasty_snack.carbs = 30

>> tasty_snack.name
=> :totopos
>> tasty_snack.carbs
=> 30
```


### Constants

Constants are all capital



### Scope resolution operator `::`
I have no idea, but I know that it's a way to access something inside a module.

e.g. using `SnackBar::SNACKS` outside of the module `SnackBar` will access the constant `SNACKS` which is inside the module SnackBar.
