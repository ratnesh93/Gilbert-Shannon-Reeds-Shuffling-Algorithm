# Gilbert-Shannon-Reeds-Shuffling-Algorithm
Implementing Gilbert-Shannon-Reeds Shuffling Algorithm and testing for Bayer &amp; Diaconis estimation for optimal shuffles at 3/2*(log2(n))

Consider a ‘deck’ to be a multiset of n cards. 
  
GSR Algorithm:
  Shuffle the deck by first cutting it into two piles according to the binomial distribution,
  join piles together by successively dropping cards from either pile with probability proportional to the size from bottom of deck
  
How to test implemtation?
  1. testing via command promt
      download the .py file and go to folder and run:
        'python GSRShufflingAlgorithm.py 26 4 20'
  2. testing via jupyter notebook
         Call 'checkingGSRImplementation(startDeckSize,n,shuffleSize)' after running previous methods
              where startDeckSize: size of staring deck
                n            : it is no. of time startDeckSize muliply by 2 , i.e 26,52,104,208, so n here is 1,2,3,4
                shuffleSize  : number fo shuffles to perform
             i.e checkingGSRImplementation(26,4,20)
  
  
