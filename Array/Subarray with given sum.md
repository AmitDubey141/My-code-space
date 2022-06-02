- [https://practice.geeksforgeeks.org/problems/subarray-with-given-sum-1587115621/1]
![image](https://user-images.githubusercontent.com/69389663/171658361-fbcb3e37-0d70-410d-9fb8-c2d433953192.png)
```py
class Solution:
    def subArraySum(self,arr, n, s): 
       #Write your code here
       
       subarr = []
       for i in range(n+1):
           for j in range(i):
               subarr.append(arr[j:i])
       #print(subarr)
       a=[]      
       for l in subarr:
           if sum(l)==s:
               for k in range(n):
                   if arr[k]== l[0]:
                       a.append(k+1)
                   if arr[k]== l[-1]:
                       a.append(k+1)
               break  
                   
       return a
```
