---
title: Hashes
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is a Hash?

A hash is a collection of elements organized in key-value pairs. the key is how you would retrieve the value
of the hash element, so unlike an array the order of the key-value pairs is arbitrary.

# What are some examples of information that would be Hashes as opposed to some other data type?

Lets say I wanted to store information about myself. I could utilize a hash to sotre information like the 
following: "age" => 28, "height" => 69, "eyes" => "blue". Another example would be having key-value pairs of 
peoples names and their ages like: {"Kyle" => 28, "Travis" => 26, "Andrea" => 24}.

# How are Hashes and Arrays similar? How are they different?

Hashes and Arrays are similar becuase they both hold collections of information which can be iterated over. 
In ruby, both hashes and arrays can hold a combination of different data types. They differ in the way you 
access information within them. In an array we would use the elements position within the array to call its 
index. In a hash, any given elements posiiton with the hash is arbitrary since we retrieve a value by providing 
the appropriate key. Each array element has a value while hashs have key-value pairs.

# How do you retrieve a particular value from a Hash?

You retrieve a value from a hash by utilizing the value's key. If I had a hash full of names and the person's 
age as key value pairs I could access a person's age by coding: my_hash["Kyle"].  This says look through the 
keys of my_hash for "Kyle" and return its value (Kyle's age).

# How do you add information to a Hash?

We add a value to an existing hash by defining the key and setting the value. If we have an existing hash, 
say my_hash, and we want to add the key-value pair "Jeff" => 58, we would code my_hash["Jeff"] = 58. If the 
key "Jeff" was not in use in the hash already it would be created with the value 58. If the key "Jeff" is 
already in the hash then its value would be changed to 58.

# How would you perform an operation on every element inside a Hash?

We would perform an operation on eahc element iside of a hash by using the each method. The each mehtod 
iterates through each element in the hash and executes some block of code. the syntax for this is:
my_hash.each{ |k, v| some code to do with each element }. Unlike an array you difing two variables for the 
code block: the key and the value (I used k and v above).

# How would you change the value of a particular element in a Hash?

Chaging the value of a hash is done by reasigning its key to the new value. Lets say I have a hash, my_hash, 
that holds key-value pairs of names of people and the key and their age as the value. A person in our hash has 
a birthday so we need to reasign the value. The birthday boy's name is "Ken". We would code my_hash["Ken"] = 68. 
This would change the value associated with the key "Ken" to 68. The other key-value pairs would go unchanged.

# How do you delete an element from a Hash?

To delete an element from a hash we could use the delete method. By using the delete method along with the key 
of the element we wish to delete we can delete the key-value pair. The syntax for this is as follows: 
my_hash.delete("Jeff"). this would delete the key-value pair from my_hash which has the key "Jeff". We can also 
do a conditional delete by using the delete_if method which will delete key-value pairs when a code block returns 
true. The code using delete_if could look like this: my_hash.delete_if { |k, v| v == number}. This says 
delete any key-value pair in my_hash in which the value of the key-value pair equals the variiable number.

# What happens if you try to retrieve an element from a Hash that does not exist in the Hash?

If you try to retrieve an element from a hash that does not exist you will be returned nil becuase there is 
nothing there matching your request.

# How do you determine how many elements are in a Hash?

to deterimine how many elements are in a hash we would use the length method. Say the hash my_hash has 3 
key-value pairs in it. the code my_hash.length would return 3 meaning there are 3 elements of key-value pairs 
in the hash.