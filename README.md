Minimum scalar product of  two vectors in Python
Here, in this page you will find the program to find the minimum scalar product of two vectors in Python Programming Language. We will discuss different methods to find the product of given two vectors.

Finding minimum scalar product of two vectors
Methods Discussed :
Method 1 : Without Using Inbuilt sort() function.
Method 2 : Using sort() function.
Method 1 :
Sort the first array in ascending order,
Sort the second array in descending order.
Declare a variable say product = 0.
Run a loop from index 0 to n
Set product += (arrr1[i]*arr2[i])
After complete iteration print product.
Time and Space Complexity :
Time Complexity : O(n2)
Space Complexity : O(1)
Method 1 : Code in Python
Run
arr1 = [1, 2, 6, 3, 7]
arr2 = [10, 7, 45, 3, 7]

n = len(arr1)

#Sort arr1 in ascending order
for i in range(n):
    for j in range(i+1, n): 
        if arr1[i]>arr1[j] :
            arr1[i], arr1[j] = arr1[j], arr1[i]

#Sort arr2 in descending order
for i in range(n):
    for j in range(i+1, n): 
        if arr2[i]<arr2[j] :
            arr2[i], arr2[j] = arr2[j], arr2[i]

product = 0
for i in range(n):
    product += arr1[i]*arr2[i]

print(product)
Output
149
Related Pages
Finding Non Repeating elements in an Array

Removing Duplicate elements from an array

Finding Maximum scalar product of two vectors in an array 

Counting the number of even and odd elements in an array 

Find all Symmetric pairs in an array 

Method 2 :
In this method we will use inbuilt sort function to sort the array.

For, sorting arr1 in ascending order, use arr1.sort()
For, sorting arr2 in descending order, use arr2.sort(reverse=True).
sort() function
The sort() method is a built-in Python method that, by default, sorts the list in ascending order.
However, you can modify the order from ascending to descending by specifying the sorting criteria.
On passing parameter reverse with value True, i.e, reverse-True : Then the array will get sorted in descending order
Minimum Scalar product in python
Method 2 : Code in Python
Run
arr1 = [1, 2, 6, 3, 7]
arr2 = [10, 7, 45, 3, 7]
n = len(arr1)

#Sort arr1 in ascending order
arr1.sort()

#Sort arr2 in descending order
arr2.sort(reverse=True)

product = 0
for i in range(n):
    product += arr1[i]*arr2[i]

print(product)
Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
Output:
149
