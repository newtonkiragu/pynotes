# Data Structures
Data structure are structures programmed to store data, so that various operations can be performed on it easily.

There are 4 built in data structures in Python - `list`, `tuple`, `dictionary` and `set`.

## List

* Holds an `ordered` collection of items.
* Can contain items of different types.
* Most versatile type of data structure in Python.
* Has no rules against unicity.
* List indices start from zero.
* `Mutable`

```python
l = ['a', 'b', 123]
```
## List Comprehensions

List comprehensions provide a concise way to create lists.
```python
l = [1, 2, 3]
new_l = [x * 2 for x in l] # [2, 4, 6]
```
### When to use lists:

>When data needs to be ordered.
When data requires the ability to be changed or extended.
When you don’t require data to be indexed by a custom value.
When you need a stack or queue.
When your data doesn’t have to be unique.

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

### When to use sets

>When you want an unordered collection of unique elements
When your data constantly changes.
When you need a collection that can be manipulated mathematically.
When you don’t need to store nested lists, sets, or dictionaries in a data structure.
When the existence of an object in a collection is more important than the order or how many times it occurs.
Use frozensets if you need both unique data and immutability.

## Tuples

* Represented by a number of values separated by commas within an optional pair of parentheses.
* `Immutable`
* Tuples are immutable, but can hold mutable objects.

```python
# constructing an empty tuple requires parentheses.
my_empty_tuple = ()

# constructing a tuple with one element requires a trailing comma.
one_elem_tuple = 'a',

#constructing a tuple with multiple elements requires a list of values separated by commas
multi_elem_tuple = 'a', 'b', [1, 2, 3]
```

### When to use tuples

> When you need to store data that doesn’t have to change.
When the performance of the application is very important. In this situation you can use tuples whenever you have fixed data collections.
When you want to store your data in logical immutable pairs, triples etc.

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

>When you need a logical association between a key:value pair.
When you need fast lookup for your data, based on a custom key.
When your data is being constantly modified