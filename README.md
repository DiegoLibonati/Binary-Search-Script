# Binary-Search-Script

## Getting Started

1. Clone the repository
2. Join to the correct path of the clone
3. Use `python binary_search.py` to execute script

## Description

I made a python script that allows to perform a binary search on a sorted list. It is necessary to emphasize that this binary search is only going to serve as I said before in ordered lists.

## Technologies used

1. Python

## Portfolio Link

`https://diegolibonati.github.io/DiegoLibonatiWeb/#/projects?q=Binary$20Search%20Script`

## Video

https://user-images.githubusercontent.com/99032604/199854535-891e68ee-ad2a-483f-b0ee-b706da9d99ed.mp4

## Documentation

`binary_search()` is used to locate an element within a list, ordered in which it begins by taking the value of its midpoint, comparing it with the value sought, so that if both do not coincide, it is determined in which of the two halves the value can be found, discarding the one in which it cannot be and repeating the process with the other, until finding said value or concluding that it is not in the list:

```
def binary_search(list_to_search, target, min_limit = None, max_limit = None):
    if min_limit == None:
        min_limit = 0
    if max_limit == None:
        max_limit = len(list_to_search) - 1

    mid_point = (min_limit + max_limit) // 2

    if max_limit < min_limit:
        return -1

    if list_to_search[mid_point] == target:
        return mid_point
    elif list_to_search[mid_point] < target:
        return binary_search(list_to_search, target, mid_point+1, max_limit)
    else:
        return binary_search(list_to_search, target, min_limit, mid_point-1)
```
