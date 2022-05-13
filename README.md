# may13-1
assn1
PROGRAM:

class Solution:
    def isPrime (self, N):
        seive=[True for i in range(N+1)]
        seive[0]=seive[1]=False
        x=int(math.sqrt(N))
        for i in range(2,x+1):
            if seive[i]:
                for j in range(i*i,N+1,i):
                    seive[j]=False
        if seive[N]:
            print('1')
        else:
            print('0')

OR

from math import sqrt
class Solution:
    def isPrime (self, N):
        # code here
        if N==1:
            return 0
        for i in range(2,int(sqrt(N)+1)):
            if N%i==0:
                return 0  # not prime
        return 1  #prime
