# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
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

#Developed by:V.S.JANANI

#RegisterNumber: 22003192


i)Use a linear search method to match the item in a list.

#Program for linear search method to match the item in a list
```
def linearsearch(array, n, k):

    for i in range(0, n):
        if (array [i] == k):
            return i
    return -1

array = eval(input())
k =  eval(input())
n = len(array)
array.sort()
result = linearsearch(array, n, k)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)        
```
     





ii)	Find the element in a list using Binary Search(Iterative Method).


#Program to find the element in a list using Binary Search(Iterative Method)..

```
def binarySearchIter(array, k, low, high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1


array=eval(input())
array.sort()
print(array)
k=eval(input()) 
low=0
high= len(array)-1
result=binarySearchIter(array, k, low, high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")
```



iii)Find the element in a list using Binary Search (recursive Method).


#Program to find the element in a list using Binary Search (recursive Method).

```
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
#sort the array
arr.sort()
print(arr)
# k is the element to be searched for
k = eval(input()) 
low=0
high=len(arr)-1
# use the binary search function to find the result
result=BinarySearch(arr, k, low, high)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")

```


## Sample Input and Output
Linear search method
![ex8py1](https://user-images.githubusercontent.com/113497340/192191163-a6241976-c947-4ae2-abe2-8a27da57df37.png)

Binary search (iterative method)
![ex8py2](https://user-images.githubusercontent.com/113497340/192191292-f5c26455-fff0-4e75-ba49-61e35b7801af.png)

Binary search (recursive method)
![ex8py3](https://user-images.githubusercontent.com/113497340/192193297-63a524f1-63bc-4d86-8ea8-1c1d84bb1012.png)







## Result
Thus the linear search and binary search algorithm is implemented using python programming.
