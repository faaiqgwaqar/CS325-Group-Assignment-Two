# CS325-Group-Assignment-Two

## Coin Change Problem
For this project, you will investigate thecoin-changeproblem:Given a cash register, how does one make change such that the fewest coins possible are returnedto the customer?  In this assignment,  we explore two algorithmic solutions to this problem:  agreedy algorithm and a dynamic programming algorithm.Formally, an algorithm for this problem should take as input:•A vectorcoinswherecoins[i] is the value of the coin of theithdenomination.•valuewhich is the amount of change we are asked to make.The algorithm should return the number of coins used to make change forvalue, and a list of the coins usedto make this value.  The objective is to minimize the number of coins returned.  In other words we want tominimizelen(coinsused).  You will implement a greedy algorithm and a dynamic programming algorithmfor this.1

## Greedy Algorithm
One approach to coin change problem is a greedy approach:•Return the largest value coin possible.•Subtract the value of this coin from the amount of change to be made.•Repeat.This implementation is calledchangegreedy.

## Dynamic Programming
We can use a dynamic programming tableTindexed by 0,1,2, . . . , valuewhereT[i] is the minimum numberof coins needed to make change fori.  Here,iis an integer such thati≥0, for the total value of currency weare making change for.T[i] =minj:coins[j]≤i{T[i−coins[j]] + 1}We initializeT[0] = 0, andT[i] =∞, fori= 1, . . . , value.  How do you store and return the coins that makethe change forvalue?  This implementation is calledchangedp
