# Linear Search and Binary search
## AIM:
To write a program to perform linear search and binary search using python programming.

## EQUIPMENT'S REQUIRED:
1.Hardware – PCs
2.Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
## Linear Search:
### Step 1:
Start from the leftmost element of array[] and compare k with each element of array[] one by one.
### Step 2:
If k matches with an element in array[] , return the index.
### Step 3:
3.If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
### Step 1:
1.Set two pointers low and high at the lowest and the highest positions respectively.
### Step 2:
2.Find the middle element mid of the array ie. arr[(low + high)/2]
### Step 3:
3.If x == mid, then return mid.Else, compare the element to be searched with m.
### Step 4:
4.If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
### Step 5:
5.Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
### Step 6:
6.Repeat steps 2 to 5 until low meets high
## PROGRAM:
i) #Use a linear search method to match the item in a list.
```python
#Program for linear search method to match the item in a list
#Developed by: Sivabalan S
#Register number: 22004401
def linearSearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
array.sort()
k = eval(input())
n = len(array)
result = linearSearch(array,n,k)
if result >=0:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found")
```
ii) # Find the element in a list using Binary Search(Iterative Method).
```python
#Program to find the element in a list using Binary Search(Iterative Method)..
#Developed by: Sivabalan S
#Register number: 22004401
def binarySearchIter(array, k, low, high):
    while(low<=high):
        mid = low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high = mid+1
    return -1
array = eval(input())
array.sort()
k = eval(input()) #k-item to be searched
result = binarySearchIter(array, k, 0, len(array)-1)
if result>=0:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found")
```
iii) # Find the element in a list using Binary Search (recursive Method).
```python
#Program to find the element in a list using Binary Search (recursive Method)..
#Developed by: Sivabalan S
#Register number: 22004401
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr,k,mid+1,high)
        else:
            return BinarySearch(arr,k,low,mid+1)
    return -1
arr = eval(input())
arr.sort()
print(arr)
k = eval(input()) 
low=0
high=len(arr)-1
result=BinarySearch(arr, k, low, high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")
```
## OUTPUT:
![output](/outpout1.png)
![output](/outpout1.png)
![output](/outpout1.png)
## RESULT:
Thus the linear search and binary search algorithm is implemented using python programming. 
