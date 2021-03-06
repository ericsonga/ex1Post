.. qnum::
   :prefix: 2-3-
   :start: 1
   
.. |checkme| image:: Figures/checkMe.png
    :height: 20px
    :align: top
    :alt: check me
    
.. |start| image:: Figures/start.png
    :height: 24px
    :align: top
    :alt: start
    
.. |finish| image:: Figures/finishExam.png
    :height: 24px
    :align: top
    :alt: finishExam
    
.. |right| image:: Figures/rightArrow.png
    :height: 24px
    :align: top
    :alt: right arrow for next page
   
Post-test Order Code Problem (Mixed Up Code)
----------------------------------------------

Construct the function ``getAverageInRange(numList, start, end)`` that takes a list of numbers, numList, and returns the average of the numbers between the start and end indices (inclusive). To do this first create a variable sum and set its initial value to 0.  Then loop from the start index to the end index (inclusive) and get the current value at the index and add it to the sum.  Check if the difference between the end index and the start index is greater than or equal to 1 and if so return the sum divided by the difference and otherwise return 0 (to prevent a divide by 0).  

Examples
=========
   
For example ``avgValuesInRange([10, 20, 30], 0, 0)`` should return 10 and ``avgValuesInRange([10, 20, 30], 1, 3)`` should return 25.
    
Order Code Here
================

Click on the |start| button below when you are ready to try to order this code.  You will have up to 10 minutes to try to solve it.  Click on the |checkme| button to check your solution.  Click on the |finish| button when you have solved this problem or wish to move on without solving it.

.. timed:: post_test_avg_values_in_range
   :timelimit: 10
   :noresult:
   :nofeedback:
   :fullwidth:
   
   .. parsonsprob:: Post_Test_Avg_Values_In_Range
      :order: 11,1,2,4,3,0,7,8,9,10,12,5,6
   
      The code below is mixed up and contains extra blocks that are not needed.  Drag the needed code from the left to the right and put them in order with the correct indention so that the code would work correctly.  
      -----
      # define function
      def avgValuesInRange(numList, start, end):
      =====
          # init sum
          sum = 0
      =====
          # init sum
          sum = 1 #paired
      =====
          # loop from start to end (inclusive)
          for index in range(start,end+1):
      ===== 
          # loop from start to end (inclusive)
          for index in range(start,end): #paired
      =====
              # get value at index
              value = numList[index]
      =====
              # get value at index
              value = index #paired
      =====
              # add value to sum
              sum = sum + value
      =====
              # add value to sum
              sum = sum + index #paired
      =====  
          # if at least one value
          if (end - start + 1) >= 1:
      =====
          # if at least one value
          if (end - start) >= 1: #paired
      =====
              # return average
              return sum / (end - start + 1)
      =====
          # otherwise return 0
          return 0

When you are finished with this problem, or are ready to move on, click the |finish| button and then go to the next page by clicking the right arrow |right| near the bottom right of this page.    
    
   
  

      
               

           
           



    