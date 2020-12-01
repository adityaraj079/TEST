# TEST

```
MCSR(A,p,r)
      1. if p==r
              return A[p]
      2. q=(p+r)/2
      3. L=MCSR(A,p,r)
      4. R=MCSR(A,q+1,r)
      5. C=left_sum()+right_sum()
return MAX(L,R,C)
```
