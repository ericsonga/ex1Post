.. qnum::
   :prefix: 4-4-
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
            

Post-test Write Code Problem
-----------------------------

Write the ``isLevelTrailSegment(elList,start,end)`` function which returns ``True`` when the trail segment is level and ``False`` otherwise.
A trail segment is defined by a starting marker, an ending marker, and all markers between those two markers (including the start and end markers). The parameters of the method are the list of elevations at the markers, the index
of the starting marker, and the index of the ending marker. The method will return true if the difference
between the maximum elevation and the minimum elevation in the trail segment is less than or equal to
10 meters.

Examples
============

For the trail shown in Figure 1 below, the trail segment starting at marker 7 and ending at marker 9 has elevations ranging from 70 to 75 meters.  Because the difference between 75 and 70 is less than 10 it is considered level.  The trail segment starting at marker 7 and ending at
marker 10 has elevations ranging between 70 and 80 meters. Because the difference between 80 and 70 is
equal to 10, the trail segment is also considered level.
The trail segment starting at marker 2 and ending at marker 12 has elevations ranging between 50 and
120 meters. Because the difference between 120 and 50 is greater than 10, this trail segment is not considered level.

.. figure:: Figures/trailMarkers.png
    :width: 600px
    :align: center
    :figclass: align-center

    Figure 1: The trail elevation as a graph and as a table

See the table below for a summary of the examples shown above.  

====== ===== =======  ====== ============  ===========
Start  End   Max      Min    Difference    is Level?
====== ===== =======  ====== ============  ===========
7      9     75       70      5			   True
7      10    80       70      10           True
2      12    120      50      70           False
====== ===== =======  ====== ============  ===========

Write Code Here
================
    
Write the ``isLevelTrailSegment(elList,start,end)`` function below so that the code compiles and passes all tests when you click the |runbutton| button.

.. activecode:: Is_level_post

   # write the isLevelTrailSegment function below
   # It should take a list of elevations, a start index, and an end index
   # It should find the minimum elevation and maximum elevation between the start and 
   # end index and return true if the difference between the maximum elevation
   # and minimum elevation between the start and end index (inclusive) is 
   # less than or equal to 10 and return false otherwise
   def isLevelTrailSegment(elList,start,end):

   # code to test the isLevelTrailSegment function
   from unittest.gui import TestCaseGui

   class myTests(TestCaseGui):

       def testOne(self):
           elevList = [100, 150, 105, 95, 95, 90, 50, 75, 75, 70, 80, 90, 100]
           self.assertEqual(isLevelTrailSegment(elevList,7,9),True,"The trail from marker 7 to 9 should be level")
           self.assertEqual(isLevelTrailSegment(elevList,7,10),True,"The trail from marker 7 to 10 should be level")
           self.assertEqual(isLevelTrailSegment(elevList,2,12),False,"The trail from marker 2 to 12 should not be level")
           self.assertEqual(isLevelTrailSegment(elevList,9,11),False,"The trail from marker 9 to 11 should not be level")
           
   myTests().main()
   
When all the tests print |pass| click the right arrow near the bottom of the page to go to the next page.
               

