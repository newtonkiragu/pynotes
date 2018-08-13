# Data Structures
Data structure are structures programmed to store data, so that various operations can be performed on it easily.

There are 4 built in data structures in Python - `list`, `tuple`, `dictionary` and `set`.

## List

* Holds an `ordered` collection of items.
* Can contain items of different types.
* Most versatile type of data structure in Python.
* Has no rules against unicity(meaning it It can contain items of different datatypes).
* List indices start from zero.
* `Mutable`

```python
l = ['a', 'b', 123]
```
## List Comprehensions

Provide a concise way to create lists.
```python
l = [1, 2, 3]
new_l = [x * 2 for x in l] # [2, 4, 6]
```
## List Operations
- Slicing a list
Returns a shallow copy of the list. The slicing indexes are optional and they work in the same way as slicing strings.
```
>>> l = ['a', 'b', 123]
>>> l[:]
['a', 'b', 123]
>>> new_l = l[1:]
>>> new_l
['b', 123]
```
- Inserting and removing elements
```
>>> l = ['a', 'b', 123]
>>> l.append(234) #inserts an element at the end of the list
>>> l
['a', 'b', 123, 234]
>>> l.insert(2, 'c') #inserts an element into the third position
>>> l
['a', 'b', 'c', 123, 234]
>>> l.insert(-1, 111) #inserts an element into the second from last position of the list (negative indices start from the end of the list)
>>> l
['a', 'b', 'c', 123, 111, 234]
>>> l.remove(111) #removes an element based on value
>>> l
['a', 'b', 'c', 123, 234]
```
- Retreiving and looking up elements
Lists can also be used as stacks or queues because of how easy it is to add and remove elements from the beginning or end of the list.
```
>>> last_element = l.pop() #returns the last element, modifying the list
>>> last_element
234
>>> l
['a', 'b', 'c', 123]
>>> third_element = l.pop(2) #returns the third element, modifying the list
>>> third_element
'c'
>>> l
['a', 'b', 123]
>>> l.index('a') 
0
```
- Whole-List Operations
```
>>> l.extend ([1, 2]) # concatenates a list on to the existing list
>>> l
['a', 'b', 123, 1, 2]
>>> l.sort()
>>> l
[1, 2, 123, 'a', 'b']
>>> l.reverse()
>>> l
['b', 'a', 123, 2, 1]
```
### When to use lists:

* When data needs to be ordered.
* When data requires the ability to be changed or extended.
* When you don’t require data to be indexed by a custom value.
* When you need a stack or queue.
* When your data doesn’t have to be unique.
* When you need a mixed collection of data.

## Sets
* `An unordered` collection of simple objects with `no duplicate` values.
* Used to eliminate duplicate values from within a list.
* All elements in a set must be hashable.
* `Mutable`

* A set can be created using the keyword set or by using curly braces {}
* To create an empty set, you have to use set() not {}; the latter creates an empty dictionary.

```python
l = [1, 2, 3]
my_set1 = set(l)
my_set2 = {1, 2, 2}
my_set3 = set() # empty set
```


## Frozenset

A regular set except that it is immutable. It is created using the keyword frozenset
```python
frozen = frozenset([1, 2, 3])
```

## Set Comprehensions
find the unique consonants within a word
```python
>>> vowels = ['a', 'e', 'i', 'o', 'u']
>>> {x for x in 'maintenance' if x not in vowels }
set(['c', 'm', 't', 'n'])
```

## Set Operations
- Joining sets
```python
>>> set1 = set([1, 2, 3])
>>> set2 = set([3, 4, 5])
>>> set1 | set2 #union
set([1, 2, 3, 4, 5])
```
- finding set intersection
```python
>>> set1 = set([1, 2, 3])
>>> set2 = set([3, 4, 5])
>>> set1 & set2 #intersection
set([3])
```
- finding set differences
```python
>>> set1 = set([1, 2, 3])
>>> set2 = set([3, 4, 5])
>>> set1 ^ set2 #symmetric difference (elements that are in the first set and the second, but not in both)
set([1, 2, 4, 5])
```
### When to use sets

* When you want an unordered collection of unique elements
* When your data constantly changes.
* When you need a collection that can be manipulated mathematically.
* When you don’t need to store nested lists, sets, or dictionaries in a data structure.
* When the existence of an object in a collection is more important than the order or how many times it occurs.
* Use frozensets if you need both unique data and immutability.

## Tuples

* Represented by a number of values separated by commas within an optional pair of parentheses.
* `Immutable`.
* Tuples are immutable, but can hold mutable objects.
* Tuples can be used as keys in dictionaries while lists cannot.
* Tuples are faster than lists.

```python
# constructing an empty tuple requires parentheses.
my_empty_tuple = ()

# constructing a tuple with one element requires a trailing comma.
one_elem_tuple = 'a',

#constructing a tuple with multiple elements requires a list of values separated by commas
multi_elem_tuple = 'a', 'b', [1, 2, 3]
```

### When to use tuples

* When you need to store data that doesn’t have to change.
When the performance of the application is very important. In this situation you can use tuples whenever you have fixed data collections.
* When you want to store your data in logical immutable pairs, triples etc.

## Dictionary

* Represented by a `key-value` pair.
* The keys can be of any immutable type and must be unique.
* The values can be of any type, mutable or immutable.
* The key-value pairs are not ordered in any manner.

* Creating a dictionary using `dict` offers less performance than using curly braces `{}`
```python
vowels = {1: 'a', 2: 'e', 3: 'i', 4: 'o', 5: 'u'}
# {1: 'a', 2: 'e', 3: 'i', 4: 'o', 5: 'u'}

{x:x*x for x in (1, 2, 3)}
# {1: 1, 2: 4, 3: 9}

dict([(1, 'a'), (2, 'e'), (3, 'i'), (4, 'o'), (5, 'u')])
# {1: 'a', 2: 'e', 3: 'i', 4: 'o', 5: 'u'}
```
### When to use a dictionary

* When you need a logical association between a `key:value` pair.
* When you need `fast lookup for your data, based on a custom key`.
* When your data is being constantly modified
