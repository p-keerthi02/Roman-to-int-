class Solution(object):
    def romanToInt(self, s):
       x={
        "I":1,
        "V":5,
        "X":10,
        "L":50,
        "C":100,
        "D":500,
        "M":1000,
       }
       N=len(s)
       output = 0
       i = 0
       while i < N:
            if i < N - 1 and x[s[i]] < x[s[i + 1]]:
                output += x[s[i + 1]] - x[s[i]]
                i += 2
            else:
                output += x[s[i]]
                i += 1
       return output
 
