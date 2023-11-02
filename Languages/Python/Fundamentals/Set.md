are like tuple but they are not ordered . They are also mutable so sets can be modified. They are like mathematical sets, there are things like intersect, union.

```python
set1 = {1,3,5,7,9,11,13,15,17,19}
set2 = {3,6,9,12,18,24}
```

### Intersect of a set
```python
set1 = {1,3,5,7,9,11,13,15,17,19}
set2 = {3,6,9,12,18,24}

intersect = set1 & set2
print(intersect) #{9, 3}
```


### Union of a set
```python
set1 = {1,3,5,7,9,11,13,15,17,19}
set2 = {2,4,6,8,10,12,14,16,18,20}

Union  = set1 | set2 
print(mod) #{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20}
```


### Difference of a set
```python
set1 = {1,2,3,4,5,6,7,8,9}
set2 = {1,2,3,4,5,6,7,8,9,10}
difference1 = set1 - set2 
difference2 = set2 - set1
print(difference1) #set(), set1 doesn't have anything that set2 doesn't have
print(difference2) #{10}, set2 has 10 which set1 doesn't have
```





### Superset and subset of a set
```python
set1 = {"Meow", "Spot"}
set2 = {"Meow"}
subset = set2 < set1 
superset = set1 > set2  
print(subset) #True since set2 is indeed a subset of set1
print(superset) #True since set 1 is the superset of set2
```



### Count the elements in a set
set = {0,1,2,3,4,5,6,7,8,9}
print(len(set)) #10

### Convert set to list
```python
set = {0,1,2,3,4,5,6,7,8,9}
print(list(set)) #[0, 1, 2, 3, 4, 5, 6, 7, 8, 9], just like normal casting
```

### Check if an element is a set
```python
set = {0,1,2,3,4,5,6,7,8,9}
print(10 in set) #False
```

