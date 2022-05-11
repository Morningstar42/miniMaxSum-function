# miniMaxSum-function
# Given five positive integers, find the minimum and maximum values that can be calculated by summing exactly four of the five integers. Then print the respective minimum and maximum values as a single line of two space-separated long integers.

!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'miniMaxSum' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def miniMaxSum(arr):
    arr.sort()
    hold = [None]*int(len(arr)-3)
    for i in range(0,len(arr)-3):
        temp = 0
        for j in range(i,i+4):
            temp = temp + arr[j]
        hold[i] = temp
    
    print(hold[0],hold[-1])

if __name__ == '__main__':

    arr = list(map(int, input().rstrip().split()))

    miniMaxSum(arr)
