Pragmatic

15. Blocks


# -> single line blocks use {} curly braces

method call  |     block
2.times        { puts "Echo" }




#Three different ways to use blocks:
#1
numbers.select do |number|
  number > 5
end

#2
numbers.select { |number| number > 5 }

#3
numbers.select { |n| n > 5 }




#More iterators: (aerie is the best name for an array, duh.)
aerie = [24, 13, 8, 65]

#select - selects according to parameter
aerie.select { |n| n > 20 }
=> [24, 65]

#reject
aerie.reject { |n| n > 20 }
 => [13, 8]

#sort
aerie.sort
 => [8, 13, 24, 65]

#reverse sort using "spaceship (<=>)"
aerie.sort { |a, b| b <=> a }
 => [65, 24, 13, 8]

#reduce - in this case sum the numbers
>> aerie.reduce {|sum, n| sum + n }
=> 110
#or
>> aerie.reduce(:+)
=> 110

#partition - evens from odds
>> evens, odds = aerie.partition { |n| n.even? }
=> [[24, 8], [13, 65]]
>> evens
=> [24, 8]
>> odds
=> [13, 65]








# Multi line blocks use do -> end
33.times do |number|
  puts "#{number} sit up"
  puts "#{number} push up"
end

# 1.upto()
1.upto(10) do |number|
  puts "#{number} sit up"
  puts "#{number} push up"
end

#in this case, "movie" is the "iterator"
@movies.each do |movie|
  movie.thumbs_up
  puts movie
end
