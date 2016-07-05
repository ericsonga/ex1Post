.. qnum::
   :prefix: 4-2-
   :start: 1

.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button
   
.. |pass| image:: Figures/pass.png
    :height: 20px
    :align: top
    :alt: pass
    
.. |fail| image:: Figures/fail.png
    :height: 20px
    :align: top
    :alt: fail

               
Post-test Fix Code Problem
----------------------------
    
The code below is trying to calculate the average rainfall, but it contains errors.  It takes a list that contains the amount of rainfall for each day, collected by a meteorologist. Her rain gathering equipment occasionally makes a mistake and reports a negative amount for that day.  Fix the code below to calculate the total rainfall by adding up all the non-negative values (including 0), also count the number of non-negative values, and return the average rainfall at the end.  Only return the average if there was at least one non-negative integer in the list, otherwise return 0.

Examples
=========

For example ``getAverageRainfall([1, 2, -3, 3])`` should ignore the -3 and sum (1 + 2 + 3) which is 6 and then divide 6 by 3 to return 2.  

Fix Code Here
==============

Fix the errors so that all the tests all print |pass| when you click the |runbutton| button. The error messages and test results are displayed below the code. 
               
.. activecode:: Rainfall_fix_post

   def getAverageRainfall(rain):
   
       # initialize the variables
       sumRain = 1
       count = 0
  
       # loop through the values in the list
       for day in Rain
           
           # if the value of day is not negative
           if day >= 0:
   
           # add the value of day to the sum and increment the count
           sumRain = sumRain + day
           count = count + 1
  
       # if count is greater than 0
       if count >= 0:

           # calculate and print the average
           ave = sumRain / count
           return ave
  
       # otherwise 
       else:
           # return 0
           return 0
       
   # code to test the getAverageRainfall function        
   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

       def testTarget(self):
           self.assertEqual(getAverageRainfall([1, 2, -3, 3]), 2)
           self.assertEqual(getAverageRainfall([-1, 2, 1, 3]), 2)
           self.assertEqual(getAverageRainfall([-1, -2, -1, -3]), 0)
           self.assertEqual(getAverageRainfall([-1, -2, 17, 13]), 15)
           self.assertEqual(getAverageRainfall([-1, 3, 17, 13, -2, 7]), 10)
           
           
   myTests().main()
           
When all the tests print |pass| click the right arrow near the bottom of the page to go to the next page.

