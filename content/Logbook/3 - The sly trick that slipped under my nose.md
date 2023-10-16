20th November 2021, Saturday

## Overview

So this is one of the trick that slipped under my nose. This tricks lowers the complexity of the solution from O(n) to O() and also to O(n)by taking advantage of the output that is the maximum sum of the question.

## Solution

```c++
// O(n^2)
int best = 0;
for(int i = 0; i < n; i++) { 
	int sum = 0; 
	for(int j = i; j < n; j++) { 
		sum += arr[j]; best = max(best, sum); 
	} 
}
```

Since we only need the best sum we only need to set best whenever we get the highest value of sum.

This goes further, check the solution below

```c++
// O(n)
int sum = 0;
int best = 0;
for(int i = 0; i < n; i++) {
	sum = max(arr[i], sum + arr[i]);
	best = max(best, sum);
}
```

In this solution I observed that the statement sum = max(arr[i], sum + arr[i]); is actually quite smart, what it does is it resets the value of sum to have a lower value if the the sum of array gets lower, this avoids polluting the sum with the values which are not the part of the sub array.

## Conclusion

The reason why this post is in the logbook is because this is obvious to me but it still slipped under my nose, so to remind my future self about this silly stuff that I forgot to think of while thinking of a solution. The O(n) was pretty smart but follows the same principle as the O(n2) i.e we only need to get the value when its highest.