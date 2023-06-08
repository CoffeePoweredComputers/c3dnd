Practice Problems
-----------------------------------------------------

Please answer
the following problems to the best of your ability without any
outside help. You can stop working on a problem after you have worked
on it for about five minutes without solving it.

Problems
==============

.. parsonsprob:: p3dnd-sum13-nd
   :adaptive:
   :numbered: left

   Create a function ``sum13(nums)`` that takes a list of numbers, ``nums`` and 
   returns the sum of the numbers in the list. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is the empty list. 
   
    .. table:: 
          :name: p3dnd-sum13-nd-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``sum13([13,1,2])``                                | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([1,13])``                                  | ``1``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([4, 13, 8])``                              | ``4``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([13, 1, 13, 3, 2])``                       | ``2``           |
          +----------------------------------------------------+-----------------+ 
   -----
   int sum13(int nums[], int size) {
   ====
     int total = 0;
     int found_13 = 0;
   ====
     for (int i = 0; i < size; i++) {
   ====
       if (found_13) {
   ====
         found_13 = 0;
   ====
       }// end if
   ====
       else if (nums[i] == 13) {
   ====
         found_13 = 1;
   ====
       } // end else if
   ====
       else {
   ====
         total += nums[i];
   ====
       } // end else
   ====
     } // end for loop
   ====

     return total;
   ====
   }


.. parsonsprob:: p3dnd-sum13-wd
   :adaptive:
   :numbered: left

   Create a function ``sum13(nums)`` that takes a list of numbers, ``nums`` and 
   returns the sum of the numbers in the list. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is the empty list. 
   
    .. table:: 
          :name: p3dnd-sum13-wd-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``sum13([13,1,2])``                                | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([1,13])``                                  | ``1``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([4, 13, 8])``                              | ``4``           |
          +----------------------------------------------------+-----------------+
          | ``sum13([13, 1, 13, 3, 2])``                       | ``2``           |
          +----------------------------------------------------+-----------------+ 
   -----
   int sum13(int nums[], int size) {
   ====
   int sum13(int nums, int size) { #paired: nums should be an array
   ====
     int total = 0;
     int found_13 = 0;
   ====
     for (int i = 0; i < size; i++) {
   ====
     for (int i = 0; i <= size; i++) { #paired: should be i < size
   ====
       if (found_13) {
   ====
         found_13 = 0;
   ====
       }// end if
   ====
       else if (nums[i] == 13) {
   ====
       elseif (nums[i] == 13) { #paired: should be else if (separated by space)
   ====
         found_13 = 1;
   ====
       } // end else if
   ====
       else {
   ====
         total += nums[i];
   ====
       } // end else
   ====
     } // end for loop
   ====

     return total;
   ====
   }

.. parsonsprob:: p3dnd-front-back-nd
   :numbered: left
   :adaptive:

   Create the function ``frontBack(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``start`` at the beginning of the string return ``"s"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``start`` at the begining and ``end`` at the end then return  ``"s_e"``.  
   * Otherwise return ``"n"``.

   For this problem you can assume that that string.h has been included.
  
   .. table:: 
      :name: p3dnd-front-back-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``frontBack("Opening time", "Open", "noon")``     | ``"s"``         |
      +----------------------------------------------------+-----------------+
      | ``frontBack("Afternoon", "Open", "noon")``        | ``"e"``         |
      +----------------------------------------------------+-----------------+
      | ``frontBack("Open at noon", "Open", "noon")``     | ``"s_e"``       |
      +----------------------------------------------------+-----------------+
      | ``frontBack("Closed", "Open", "noon")``           | ``"n"``         |
      +----------------------------------------------------+-----------------+
      | ``frontBack("It is noon now", "open", "noon")``   | ``"n"``         |
      +----------------------------------------------------+-----------------+
   -----
   char* frontBack(char* str, char* start, char* end) {
   =====
       if (strncmp(str, start, strlen(start)) == 0 && strcmp(str - strlen(end), end) == 0) {
   =====
           return "s_e";
   =====
       } else if (strncmp(str, start, strlen(start)) == 0) {
   =====
           return "s";
   =====
       } else if (strcmp(str + strlen(end), end) == 0) {
   =====
           return "e";
   =====
       } else {
   =====
           return "n";
   =====
       }
   =====
   }

.. parsonsprob:: p3dnd-front-back-wd
   :numbered: left
   :adaptive:

   Create the function ``front_back(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``start`` at the beginning of the string return ``"s"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``start`` at the begining and ``end`` at the end then return  ``"s_e"``.  
   * Otherwise return ``"n"``.
  
   .. table:: 
      :name: p3dnd-front-back-wd-table
      :widths: 70 30
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``front_back("Opening time", "Open", "noon")``     | ``"s"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Afternoon", "Open", "noon")``        | ``"e"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Open at noon", "Open", "noon")``     | ``"s_e"``       |
      +----------------------------------------------------+-----------------+
      | ``front_back("Closed", "Open", "noon")``           | ``"n"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("It is noon now", "open", "noon")``   | ``"n"``         |
      +----------------------------------------------------+-----------------+
   -----
   char* frontBack(char* str, char* start, char* end) {
   =====
   char frontBack(char* str, char* start, char* end) { #paired: should be char* as a string is being returned
   =====
       if (strncmp(str, start, strlen(start)) == 0 && strcmp(str - strlen(end), end) == 0) {
   =====
           return "s_e";
   =====
       } else if (strncmp(str, start, strlen(start)) == 0) {
   =====
           return "s";
   =====
       } else if (strcmp(str - strlen(end), end) == 0) {
   =====
           return "e";
   =====
       } else {
   =====
           return "n";
   =====
       }
   =====
   }


.. parsonsprob:: p3dnd-bob-there-nd
   :numbered: left
   :adaptive:

   Create a function, ``bobThere(str)`` that takes a string, ``str``. It returns ``True`` if ``str`` contains 
   a "bob" string, but where the
   middle 'o' char can be any char. Otherwise it returns ``False``.

   .. table:: 
      :name: p3dnd-bob-there-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``bobThere("abcbob")``            | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("b9b")``               | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("bac")``               | ``False``                             |
      +----------------------------------+---------------------------------------+
   -----
   bool bobThere(char* str) {
   =====
       for (int i = 0; i < string_length(str) - 2; i++) {
   =====
           if (str[i] == 'b' && str[i + 2] == 'b') {
   =====
               return true;
   =====
           } // end if
   =====
       } // end for loop
   =====
       return false;
   =====
   } // end bobThere

.. parsonsprob:: p3dnd-bob-there-wd
   :numbered: left
   :adaptive:

   Create a function, ``bobThere(str)`` that takes a string, ``str``. It returns ``True`` if ``str`` contains 
   a "bob" string, but where the
   middle 'o' char can be any char. Otherwise it returns ``False``.

   .. table:: 
      :name: p3dnd-bob-there-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``bobThere("abcbob")``            | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("b9b")``               | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``bobThere("bac")``               | ``False``                             |
      +----------------------------------+---------------------------------------+
   -----
   bool bobThere(char* str) {
   =====
   bobThere(char* str) { #paired: return type should be bool
   =====
       for (int i = 0; i < string_length(str) - 2; i++) {
   =====
       for (int i = 0; i < string_length(str) - 2; i++) { # paired: need to iterate over the length minus 2 so as not to go out of bounds
   =====
           if (str[i] == 'b' && str[i + 2] == 'b') {
   =====
           if (str[i] == 'b' && str[i] == 'b') { # paired: Needs to check if the first and last letter are b
   =====
               return true;
   =====
           } // end if
   =====
       } // end for loop
   =====
       return false;
   =====
   } // end bobThere

.. parsonsprob:: p3dnd-palindrome-number-nd
   :numbered: left
   :adaptive:

   Create a function ``isPalindrome(x)`` that takes an integer, ``x``, and returns 
   ``True`` if x is a palindrome , and ``False`` otherwise.   An integer is a palindrome 
   if the digits read the same backwards as forwards.

   .. table:: 
      :name: p3dnd-palindrome-number-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``isPalindrome(121)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(888)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(678)``             | ``[]``                                |
      +----------------------------------+---------------------------------------+
   -----
   int isPalindrome(int number) {
   =====
     int temp = number;
     int reversedNumber = 0;
   =====
     while (temp > 0) {
   =====
       reversedNumber = reversedNumber * 10 + temp % 10;
   =====
       temp /= 10;
   =====
     } // end while
   =====
     if (reversedNumber == number) {
   =====
       return true; 
   =====
     } else {
   =====
       return false; 
   =====
     } // end else
   =====
   }

.. parsonsprob:: p3dnd-palindrome-number-wd
   :numbered: left
   :adaptive:

   Create a function ``isPalindrome(x)`` that takes an integer, ``x``, and returns 
   ``True`` if x is a palindrome , and ``False`` otherwise.  An integer is a palindrome 
   if the digits read the same backwards as forwards.

   .. table:: 
      :name: p3dnd-palindrome-number-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``isPalindrome(121)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(888)``             | ``True``                              |
      +----------------------------------+---------------------------------------+
      |``isPalindrome(678)``             | ``[]``                                |
      +----------------------------------+---------------------------------------+
   -----
   int isPalindrome(int number) {
   =====
   isPalindrome(int number) { #paired: missing return type
   =====
     int temp = number;
     int reversedNumber = 0;
   =====
     while (temp > 0) {
   =====
     while (temp < 0) { #paired: temp should be greater than 0
   =====
       reversedNumber = reversedNumber * 10 + temp % 10;
   =====
       reversedNumber = reversedNumber * 100 + temp % 10; #paired: reversedNumber should be multiplied by 10
   =====
       temp /= 10;
   =====
       temp / 10; #paired: integers divides but does not store the result in temp
   =====
     } // end while
   =====
     if (reversedNumber == number) {
   =====
       return true; 
   =====
     } else {
   =====
       return false; 
   =====
     } // end else
   =====
   }
