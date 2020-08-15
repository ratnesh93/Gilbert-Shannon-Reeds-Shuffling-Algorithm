# Gilbert-Shannon-Reeds-Shuffling-Algorithm
Implementing Gilbert-Shannon-Reeds Shuffling Algorithm and testing for Bayer and Diaconis estimation for optimal shuffles at 3/2*(log2(n))
Optimal shuffle is minimum shuffle required to fully randomized the cards

Consider a ‘deck’ to be a multiset of n cards. 
  
GSR Algorithm:
  Shuffle the deck by first cutting it into two piles according to the binomial distribution,
  join piles together by successively dropping cards from either pile with probability proportional to the size from bottom of deck
  
How to test implemtation?
  1. testing via command promt
      download the .py file and go to folder and run:
        'python GSRShufflingAlgorithm.py 26 4 20'
        when a image plot will open, close first to see for second and so on
  2. testing via jupyter notebook
         Call 'checkingGSRImplementation(startDeckSize,n,shuffleSize)' after running previous methods
              where startDeckSize: size of staring deck
                n            : it is no. of time startDeckSize muliply by 2 , i.e 26,52,104,208, so n here is 1,2,3,4
                shuffleSize  : number fo shuffles to perform
             i.e checkingGSRImplementation(26,4,20)
  
  
Reporting Findings:
  After looking at plots we can see that after few shuffles there is steep increase in the graph after which the randomness values donot change much
  So we can assume that after steep change or we can say where we can find 'elbow' in the graph, that is minimum amount of shuffles required to fully randomized the   cards.
  
  Deck Size         Minimium Shuflle as per Bayer and Diaconis(3/2*(log2(n))        Shuffle where Elbow In Graph
  26                4                                                               4-5
  52                8                                                               8-9 
  104               10                                                              10-11
  208               11                                                              10-11
  
  So after observing above results we can say that (3/2*(log2(n)) is a good approximation for optimal number of shuffles
  
  implemenation of shuffle method is such a way that new random getting #get_random_number_for_right_deck(n) and #should_drop_from_right_deck(n_left, n_right) can   be passed
