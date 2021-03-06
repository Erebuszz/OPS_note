* noted by Erebuszz, modified on 5/13/2017

* Excerpts from << Python 101 >>

# The <b>for</b> Loop

## The <b>range</b> function

> <b>xrange</b> in Python 2.x

* Create a list that is n in length

```python
print(range(5))
print(range(5, 10))
print(range(2, 10, 3))  # (start, end-1, step)
```
Output

    [0, 1, 2, 3, 4]
    [5, 6, 7, 8, 9]
    [2, 5, 8]

Combine with the loop function

```python
for num in range(1, 10, 3):
    print(num)
```
Output

    1
    4
    7

> Use <b>comma (,)</b> after print statement if you don't want a new line after it

Also works for a dictionary

```python
a_dict = {"one": 1, "two": 2, "three": 3}
for key in a_dict:  # same as a_dict.keys()
    print(key)
```
Output

    three
    two
    one

Sort before iterate over them

```python
a_dict = {1: "one", 2: "two", 3: "three"}
keys = a_dict.keys()
keys.sort()
for key in a_dict:
    print(key)
```
Output

    1
    2
    3

# The <b>while</b> Loop

```python
i = 0
while i < 10:
    print(i)
    if i == 5:
        break
    i += 1  # i = i + 1
```
Output

    0
    1
    2
    3
    4
    5

> Use <b>break</b> to break out of a loop

> Use <b>continue</b> to skip an iteration or continue with the next iteration

```python
i = 0
while i < 10:
    if i == 3:
        i += 1
        continue
    print(i)
    if i == 5:
        break
    i += 1  # i = i + 1
```
Output

    0
    1
    2
    4
    5

# What else is for in loops

> The <b>else</b> statements only execute if the loop completes successfully

The primary use is for searching items

```python
my_list = [1, 2, 3, 4, 5]

for num in my_list:
    if(num == 10):
        print("Item found!")
        break
    print(num)
else:
    print("Item not found!")
```
Output

    1
    2
    3
    4
    5
    Item not found!