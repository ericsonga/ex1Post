.. qnum::
   :prefix: 4-3-
   :start: 1
   
.. |checkme| image:: Figures/checkMe.png
    :height: 20px
    :align: top
    :alt: check me
   
Post-test Order Code Problem (Mixed Up Code)
---------------------------------------------

Construct the function ``getLenLongestRun`` that takes a list of numbers and returns the length of the longest run in the list of numbers.  A run of numbers is when two or more numbers that are adjacent in a list have the same value.  If there are no runs in the list then return 1. 

To calculate the length of longest run create a variable to track the current length and the longest length and initialize them both to 0.  Then  loop through the indicies of the list from 0 to one before the last index and compare the value at the current index to the value at the next index. If they are the same then increment the current length.  If the current length is greater than the max length then set the max length to the current length. If the value at the current index and the next index are not the same set the current length to 0.  Return the longest length plus one (since you only count 1 when you find the first pair).

Examples
=========
   
In the image below there are two runs of length 4.  One starts at index 6 and one at index 14.  

.. figure:: Figures/longestRun2.png
    :width: 600px
    :align: center
    :figclass: align-center

    Figure 1: A list of numbers with two runs of length 4.  One starts at index 6 and one at index 14. 
    
Order Code Here
================
   
.. parsonsprob:: longestRun_post
   :order: 5,4,12,11,9,6,0,8,7,1,10,3,2
   
   The code below is mixed up and contains extra blocks that are not needed.  Drag the needed code from the left to the right and put them in order with the correct indention so that the code would work correctly.  
   -----
   def getLenLongestRun(numList):
   =====
       currentLen = 0
       longestLen = 0
   =====
       for index in range(len(numList)-1):
   ===== 
       for index in range(len(numList)): #paired
   =====
           if numList[index] == numList[index+1]:
   =====
           if index == index + 1: #paired
   =====
               currentLen = currentLen + 1      
               if currentLen > longestLen:
   =====
                   longestLen = currentLen
   =====
                   currentLen = longestLen #paired
   =====
           else:
   =====
               currentLen = 0
   =====  
       return longestLen + 1
   =====
       return longestLen #paired

   
When you click the |checkme| button and "Perfect!" is printed then click the right arrow near the bottom of the page to go to the next page.     
  

   
