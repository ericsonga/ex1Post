.. qnum::
   :prefix: 4-1-
   :start: 1
   
.. |start| image:: Figures/start.png
    :height: 24px
    :align: top
    :alt: start
    
.. |next| image:: Figures/next.png
    :height: 24px
    :align: top
    :alt: next
    
.. |prev| image:: Figures/prev.png
    :height: 24px
    :align: top
    :alt: prev
    
.. |finish| image:: Figures/finishExam.png
    :height: 24px
    :align: top
    :alt: finishExam
   
Post-test Multiple-Choice Questions
------------------------------------

Please answer the following multiple-choice questions to the best of your ability.  Click the |start| button when you are ready to begin the exam.  This will display one multiple-choice question.  Click on the radio button next to the best answer and then click on the |next| button below the question to display the next question.     Click on the |prev| button to go back to the previous question. Use the number buttons to jump to a particular question.     
When you have answered all of the multiple-choice questions click on the |finish| button which is in the center near the bottom of this page. 

.. timed:: post-test
   :noresult:
   :nofeedback:
   :notimer:
       
   .. mchoice:: post1
      :answer_a: I.
      :answer_b: II.
      :answer_c: III.
      :answer_d: IV.
      :answer_e: V.
      :correct: b
      :feedback_a: What happens if the last two values are in ascending order, but other values are not?
      :feedback_b: This only returns false when it finds list values that are not sorted in ascending order.
      :feedback_c: When does this return true?
      :feedback_d: This returns true when at least one list value is greater than the next one (next highest index) does that mean that the list is sorted in ascending order?
      :feedback_e: This returns true when at least one list value is greater than the next one (next highest index) does that mean that the list is sorted in ascending order?

      The following function ``isSorted`` should only return true if the values in ``numList`` are sorted in ascending order (with ``numList[i]`` less than or equal to ``numList[i+1]`` for all i). Otherwise, the function should return false.  Which of the following can be used for the "missing code" to make the function work correctly?
       
      ::
          
           def isSorted(numList):
           
               // missing code

               
           I.
               b = True
      	       for i in range(len(numList) - 1):
                   if numList[i] > numList[i+1]:
                       b = False
                   else:
                       b = True
               return b
               
          II.
              for i in range(len(numList) - 1):
                  if numList[i] > numList[i+1]:
                      return False
              return True
              
          III.
              b = False
              for i in range(len(numList) - 1):
                  if numList[i] > numList[i+1]:
                      b = False
              return b
              
          IV. 
              b = False
              for i in range(len(numList) - 1):
                  if numList[i] > numList[i+1]:
                      b = True
              return b	
		      
          V.  
              for i in range(len(numList) - 1):
                  if numList[i] > numList[i+1]:
                      return True
              return False
		      

   .. mchoice:: post2
      :answer_a: It is the length of the shortest consecutive block of the value target in nums
      :answer_b: It is the length of the array nums
      :answer_c: It is the length of the first consecutive block of the value target in nums
      :answer_d: It is the number of occurrences of the value target in nums
      :answer_e: It is the length of the last consecutive block of the value target in nums
      :correct: d
      :feedback_a: It doesn't reset lenCount ever, so it just counts all the times the target value appears in nums.
      :feedback_b: It only increments the lenCount when the current num is equal to the target.
      :feedback_c: It doesn't reset lenCount ever, so it just counts all the times the target value appears in the array.
      :feedback_d: The variable lenCount is incremented each time the current array element is the same value as the target. It is never reset so it counts the number of occurrences of the value target in nums. The method returns maxLen which is set to lenCount after the loop finishes if lenCount is greater than maxLen.
      :feedback_e: It doesn't reset lenCount ever, so it just counts all the times the target value appears in the array.

      Consider the following function ``findLongest`` which is intended to find the longest consecutive block of the value ``target`` occurring in the list ``nums``; however ``findLongest`` does not work as intended.  For example, if the list ``nums`` contains the values [7, 10, 10, 15, 15, 15, 15, 10, 10, 10, 15, 10] the call ``findLongest(10, nums)`` should return 3, the length of the longest consecutive block of 10s.  Which of the following best describes the value actually returned by a call to ``findLongest``?  
       
      ::
               
           def findLongest(target, nums):
               lenCount = 0
               maxLen = 0
               for num in nums:
                   if num == target:
                       lenCount = lenCount + 1
                   else:
                       maxLen = lenCount
               if lenCount > maxLen:
                   maxLen = lenCount
               return maxLen
               
   .. mchoice:: post3
      :answer_a: 26
      :answer_b: 165
      :answer_c: 139
      :answer_d: 164
      :answer_e: 165
      :correct: c
      :feedback_a: This adds up every other number starting with the one at index 1 (second in list).
      :feedback_b: This adds up every other number starting with the one at index 1 (second in list).
      :feedback_c: This adds up every other number starting with the one at index 1 (second in list).
      :feedback_d: This adds up every other number starting with the one at index 1 (second in list).
      :feedback_e: That is okay.  We do not expect you to know this.

      Given the following code segment, what will be printed when this code is executed (run)?
       
      ::

          sum = 0 # Start out with nothing
          thingsToAdd = [1,3,4,5,21,131]
          for number in range(1,len(thingsToAdd),2):
              sum = sum + thingsToAdd[number]
          print(sum)
          
   .. mchoice:: post4
      :answer_a: 4
      :answer_b: 2
      :answer_c: 16
      :answer_d: 7
      :answer_e: 3
      :correct: b
      :feedback_a: This would be true if I asked what was printed
      :feedback_b: This function subtracts one from every value in the list.  Returning numList[1] * 2 does not change what is in numList.
      :feedback_c: This would be true if lists started with index 1 and I asked what was printed.
      :feedback_d: This would be true if lists started with index 1.
      :feedback_e: The value at index 1 is decremented by 1.  

      Given the following function definition, what will be the value in ``numList[1]`` after ``mystery(numList)`` is executed (run)?
      ::

          def mystery(numList):
              for index in range(len(numList)):
                  numList[index] = numList[index] - 1
              return numList[1] * 2
            
          numList = [8, 3, 1]
          print(mystery(numList))
          
   .. mchoice:: pt5
      :answer_a: a = 11 and b = 2
      :answer_b: a = 12 and b = 1
      :answer_c: a = 3 and b = 11
      :answer_d: a = 8 and b = 5
      :answer_e: a = 5 and b = 8
      :correct: e
      :feedback_a: This would be true if it was range(1,3).
      :feedback_b: This would be true if it was range(1,5).  Remember that range doesn't include the second value.
      :feedback_c: Not quite.  Check your tracing.
      :feedback_d: Not quite.  Check your tracing.  
      :feedback_e: Good job tracing this! 

      What do ``a`` and ``b`` equal after the following code executes?
      ::

          a = 10
          b = 3
          t = 0
          for i in range(1,4):
              t = a;
              a = i + b;
              b = t - i;
              
   .. mchoice:: post6
      :answer_a: Whenever the first element in numList is equal to target
      :answer_b: Whenever numList contains any value equal to target
      :answer_c: Whenever more than one value in numList is equal to target
      :answer_d: Whenever exactly one value in numList is equal to target
      :answer_e: Whenever the last value in numList is equal to target
      :correct: c
      :feedback_a: No
      :feedback_b: No
      :feedback_c: Yes
      :feedback_d: No 
      :feedback_e: No

      Given the following code which of the following answers best describes the conditions for mystery to return true?
      ::
          def mystery(numList, target):
              temp = False
              count = 0
              for value in numList:
                  if value == target:
                      count = count + 1
              temp = count > 1
              return temp 
              
After you finished this test go to the next page by clicking the right arrow near the bottom right of this page. 