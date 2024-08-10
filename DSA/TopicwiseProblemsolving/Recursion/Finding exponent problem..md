#leetcode #recursion [link](https://leetcode.com/problems/powx-n/) 

## Problem:
Implement [pow(x, n)](http://www.cplusplus.com/reference/valarray/pow/), which calculates `x` raised to the power `n` (i.e., `xn`).

**Example 1:**

**Input:** x = 2.00000, n = 10
**Output:** 1024.00000

**Example 2:**

**Input:** x = 2.10000, n = 3
**Output:** 9.26100

**Example 3:**

**Input:** x = 2.00000, n = -2
**Output:** 0.25000
**Explanation:** 2-2 = 1/22 = 1/4 = 0.25

**Constraints:**

- `-100.0 < x < 100.0`
- `-231 <= n <= 231-1`
- `n` is an integer.
- Either `x` is not zero or `n > 0`.
- `-104 <= xn <= 104`

<hr>

## Solution:
### Approach 1: Brute Force Method

This worked for most but failed when the value of n was too large. This solution uses a simple O(n) recursive algorithm and uses the helper class  to help with the negative exponents. This is basically how we would do it normally in a loop as well.

```C++
class Solution {
	double helper(double x, int n){
	    if(n == 0) return 1;
	    else return x * helper(x,--n);
	}

	public double myPow(double x, int n){
	    int flag = 0;
	    if(n < 0){
	        flag++;
	    }
	    if(flag == 1) n *= -1;
	    double res = helper(x,n);
	    if(flag == 1) return 1.0/res;
	    else return res;
	}
}
```

### Approach 2: Binary Exponentiation

#chatgpt Binary exponentiation is O(log n) time complexity that uses the following mathematical properties of exponents to calculate the exponent.

$$
a^n = \begin{cases} 1, & \text{if } n = 0 \\ a^{n/2} \times a^{n/2}, & \text{if } n \text{ is even} \\ a \times a^{(n-1)/2} \times a^{(n-1)/2}, & \text{if } n \text{ is odd} \end{cases}
$$

Since we cut down the exponent by 2 in every iteration, we get a O(log$_2$n) algorithm which is much faster and covers all the cases.

```C++
double helper(double x, int n){
    //0 power
    if(n == 0) return 1;
        double ans = helper(x,n/2);
    if(n % 2 == 0){
        return ans * ans;
    }else{
        return x * ans * ans;
    }
}

double myPow(double x, int n) {
    int flag = 0;
    // takes care of -ve exponent
    if(n < 0){
        flag++;
        n *= -1;
    }
    double res = helper(x,n);
    if(flag == 1) return 1/res;
    else return res;
}
```
