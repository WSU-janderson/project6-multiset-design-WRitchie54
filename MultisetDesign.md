# Introduction

In this document I will discuss the creation of an RPG game inventory system using MultiSet design with a Sequence\<"string">. The string will represent an ID of an item in the game world. This ID is mapped to another system for item qualities such as stat modifiers, value, and item type.

# Design Philosophy

My main reason for utilizing a Sequence as my MultiSet basis is for the simplicity and ease of readability for other developers when working with it. Other developers will use this multiset when programming character functions in the game as the inventory is very closely tied with characters. It will also be used with the item ID mapping system so that items can have large property sets.


# Core Operations (Add edge cases if not present)

Any Multiset design is going to need to do a handful of operations to be able to be used properly. Below are a couple of the operations needed.

## Operation 1

One of the first major operations needed for the inventory system is the capability to add new items to the inventory. This is necessary for when a character picks up loot, purchases items from a vendor or when the character trades with another player. This is directly supported through the Sequence. It will have a time complexity of O(1) as all insertions will happen as push_backs at the end of the list. 

## Operation 2

Another major operation needed for the inventory system is the capability to remove an item from the inventory. This would be needed when a character uses a disposable item, sells something to another character or drops an item on the ground. This is directly supported with a Sequence and will have a worst-case time complexity of O(n) this is because the item needs to be found in the sequence and if it is the last item it has to go through every other item first to find a match.

## Operation 3

Getting a quantity count of how many of a single item is in the inventory is also essential. This would be used when showing how many of an item like a potion the character has. The time complexity of this is O(n) as one needs to go through entire list to add up all of the instances of the item. This operation is slow for an extremely large inventory but I do not expect item amounts in an inventory to become large enough for awful performance to be had.

## Operation 4

A final major operation needed is access to how large the inventory currently is. This would be obtained by taking the index of the last element in the Sequence and adding 1. This results in an O(1) time complexity.

# Set Operations

A useful set operation for my game inventory would be (). This could be useful in (). It would be implemented via .... 

# Extension Feature

# UML Diagram

# Trade-off Analysis
|   |   |
|---|---|
|   |   |

# Alternative Design Sketch

# Evaluation Plan

To fully evaluate the (data structure) a set of tests would need developed to show proper functionality. These tests would consist of ...

# Conclusion

# References
