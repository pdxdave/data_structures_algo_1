# data_structures_algo_1

Python does not have a static array data type. However, '''Lists''' are built on dynamic arrays.     
An array is a data structure that organizes items sequentially. Each position in an array has an index. The first position in an array has an index of 0.

- Search 0(1): To look up an item by index in an array is constant time (O(1).    
- Add 0(1): Adding an item to the end of an array is constant time (O(1)).
- Insert 0(n): In the worst case, inserting an item in an array is linear time (O(n)). When you insert into an array, all the items — starting at the index we are inserting into have to be shifted one index.
- Delete 0(n): In the worst case, deleting an item in an array is linear time (O(n)). For any item you delete (unless it is the last item), all of the items after that index have to be shifted over to fill the now blank spot in the array. 
