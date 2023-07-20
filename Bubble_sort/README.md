**Bubble Sort effect looks like that effect when you throw a stone in water so the heavy stone goes down in water and bubbles created goes up as they are light**

  


## explanation:

- imagine we have the list [8, 5, 7, 3, 2] the logic is simple go through elements compare and if bigger swap !
you can clearly infer what would happen 8 will move along the list to the end and voila we found the biggest element !
[5, 7, 3, 2, 8]
(that's a good technique to find the biggest element in a list) now we can repeat this process using the remaining elements and so on !

- every pass(iteration) of bubble sort produces getting one new heaviest element so if we want out of list of n numbers the largest k numbers in that list we can perform k bubble sort iterations !

- based on the previous observation if we want to sort n numbers we need to know the heaviest n - 1 elements of those numbers so we need n - 1 iteration(passes) of bubble sort to sort n elements

  

we perform n - 1 (linear) passes in every pass we iterate through list of elements that shrinks but shrinks linearly 4 -> 3 -> 2 -> 1

*i can clearly say it's O(n^2) linear operations of linear operations !*

**another approach :)**

- if we have 4 elements we would have 3 passes every pass operations shrinks linearly 3 + 2 + 1 operations
but if we have n elements ?
would have n - 1 passes and every pass operations shrinks linearly n - 1 + .... + 3 + 2 + 1 using sum formula we get
n*(n - 1)/2 which is of order n^2 !

  

## pseudo code time!

  

```
function bubbleSort(list, listLength)
{
    for (i = 0; i < n-1; i++)
    {
        flag = 0
        for (j = 0; j<n-1-j; j++)
        {
            if (list[j] > list[j + 1])
            {
                swap(list[j], list[j + 1]);
                flag = 1
            }
        }
        if (flag == 0)
            break;
    }
}
```

*what about that flag variable ?*
**it's for adaptability!**

  

1) Number of comparisons -> O(n^2)

2) Number of swaps -> O(n^2)

3) Adaptive : if we applied bubble sort to a sorted list it would go for one iteration only and know the flag didn't change then will break and finish!

4) Stablbe: it's a stable algorithms as in case of equal elements it keeps the original sorting and not swapping, it only swaps in case of (bigger than >)

5) Memory: no extra memory needed just the original list to be sorted
