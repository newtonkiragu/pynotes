# Unit testing

A method by which individual units of code are scrutinized to determine if they are fit for use.

#### Test fixture
Represents the preparation needed to perform one or more tests, and any associate cleanup actions. e.g. creating temporary or proxy databases.

#### Test case
The individual unit of testing. It checks for a specific response to a particular set of inputs.

#### Test suite
A collection of test cases.

#### Test runner
A component which orchestrates the execution of tests and provides the outcome to the user. The test runner may use a graphical interface, a textual interface, or return a special value to indicate the results of executing the tests.

> The `unittest` module provides a rich set of tools for constructing and running tests.

Example:

```python
import unittest
from fizzbuzz import fizz_buzz

class TestFizzBuzzMethod(unittest.TestCase):
	"""Tests behaviors of the ```fizz_buzz`` method."""
	def test_fizz(self):
		self.assertEqual(fizz_buzz(3), 'Fizz')

	def test_buzz(self):
		self.assertEqual(fizz_buzz(5), 'Buzz')

if __name__ == '__main__':
	unittest.main()
```
A testcase is created by subclassing `unittest.TestCase`. Tests methods name's start with the letters `test`. This naming conventions informs the test runner about which methods represent tests.

In order to test something, we use one of the assert() methods provided by the TestCase base class. If the test fails, an exception will be raised, and unittest will identify the test case as a failure.

[list of assert methods](#list-of-assert-methods)

> `unittest.main()` provides a command-line interface to the test script.

Run: `$ python fizzbuzz_test.py`

The above script produces an output like this:

```
..
----------------------------------------------------------------------
Ran 2 tests in 0.000s

OK
```

The `setUp()` and `tearDown()` methods allow you to define instructions that will be executed before and after each test method.

The unittest module can be used from the command line to run tests from modules, classes or even individual test methods.

> Use `python -m unittest -h` for a list of all the command-line options

You can run tests with more detailed information by passing in the verbosity argument:

```python
if __name__ == '__main__':
    unittest.main(verbosity=2)
```
[Nose](https://nose.readthedocs.org/en/latest/) and [py.test](http://pytest.org/)  are third-party unittest frameworks with a lighter-weight syntax for writing tests.

### list-of-assert-methods

| Method |Checks that |New in |
| ----|:---:|---:|
assertEqual(a, b)|a == b|   |
assertNotEqual(a, b)|	a != b|
assertTrue(x)|	bool(x) is True|
assertFalse(x)|	bool(x) is False|
assertIs(a, b)|	a is b|	3.1
assertIsNot(a, b)|	a is not b|	3.1
assertIsNone(x)|	x is None|	3.1
assertIsNotNone(x)|	x is not None|	3.1
assertIn(a, b)|	a in b|	3.1
assertNotIn(a, b)|	a not in b|	3.1
assertIsInstance(a, b)|	isinstance(a, b)|	3.2
assertNotIsInstance(a, b)|	not isinstance(a, b)|	3.2

[Python docs](https://docs.python.org/3/library/unittest.html)
