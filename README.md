# data_structures_algo_1

## Array and String Manipulation

### Static Arrays
Python does not have a static array data type. However, ```Lists``` are built on dynamic arrays.     
An array is a data structure that organizes items sequentially. Each position in an array has an index. The first position in an array has an index of 0.

- Search 0(1): To look up an item by index in an array is constant time (O(1).    
- Add 0(1): Adding an item to the end of an array is constant time (O(1)).
- Insert 0(n): In the worst case, inserting an item in an array is linear time (O(n)). When you insert into an array, all the items — starting at the index we are inserting into have to be shifted one index.
- Delete 0(n): In the worst case, deleting an item in an array is linear time (O(n)). For any item you delete (unless it is the last item), all of the items after that index have to be shifted over to fill the now blank spot in the array. 
- Space 0(n): The space complexity of an array is linear (O(n)). Each item in the array will take up space in memory.

#### Stengths: Static arrays are great because they allow fast lookups and fast appends 0(1). 
#### Weaknesses: The primary weakness of a static array is that it has a fixed size. Another weakness is the linear time insertions and deletions

- Slicing an array cost: you are actually allocating a new list. Second, you copy all of the items in your slice from the original array into the newly allocated list. This means that you have an O(n) time cost (for the copying) and an O(n) space cost for the newly allocated list.    

### in-place vs out-of-place algorithms. 

- in-place: In general these create additional variables that are 0(1) space.  The do have side effects though.  Only use them if you are space constrained.
```

def test_me(num_list):
  for idx, item in enumerate(num_list):
    num_list[idx] += 2

num_list = [1,2,3]
test_me(num_list)
print(num_list)
```

- out-of-place: The better choice. They copy the data structures or objects before manipulating them.
```
def test_me(num_list):

  doing_it = [None] * len(num_list)     // new var holding data

  for idx, item in enumerate(num_list): // loop through input
    doing_it[idx] = item * 2            // add results to new var

  return doing_it                       // return new var

num_list = [1,2,3]
num_list = test_me(num_list)
print(num_list)                         // print results of new var
```


