# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
# step1: 
Use def to assign the variables.
# step2:
by using elif clause
# step3:
give input through arr and eval 
# step4:
and then print to find the element whether the element is found or not.

## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
Program for linear search method to match the item in a list
Developed by: Chandana Yendluri
RegisterNumber: 23011258
'''
def linearsearch(array,n,k):
    for i in range (0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
k = eval(input()) # k-item to be seared for
n=len(array)
array.sort()
result = linearsearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```
## input and output:
![image](https://github.com/Tanessha/Search-Algorithm/assets/140876194/d1ea23a1-449c-47e1-83c4-a48fdf254bac)


ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Chandana Yendluri
RegisterNumber: 23011258
'''
def binarysearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input())
result=binarysearchIter(array, k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
## input and output:
![image](https://github.com/Tanessha/Search-Algorithm/assets/140876194/4df70777-f196-4fdf-8572-eaeaf8efe77c)


iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Chandana Yendluri
RegisterNumber:23011258 
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid+1,high)
    else:
            return -1
arr = eval(input())
arr.sort()
k = eval(input()) 
result=BinarySearch(arr, k,0,len(arr)-1)
if(result==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
## Sample Input and Output
![image](https://github.com/Tanessha/Search-Algorithm/assets/140876194/08dd1d58-020e-4e06-8a75-24695ffc69d1)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
