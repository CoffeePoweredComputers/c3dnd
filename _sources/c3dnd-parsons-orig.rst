Practice Problems
-----------------------------------------------------

Please answer
the following problems to the best of your ability without any
outside help. You can stop working on a problem after you have worked
on it for about five minutes without solving it.

Problems
==============

.. parsonsprob:: c3dnd-sum13-nd
   :adaptive:
   :numbered: left
   :language: c++

   Create a function ``sum13(nums)`` that takes a list of numbers, ``nums`` and 
   returns the sum of the numbers in the list. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is the empty list. 
   
   .. table:: 
         :name: c3dnd-sum13-nd-table
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
   #include &lt;stdio.h&gt;
   =====
   int sum_13(int* nums, int length) {
   =====
       int total = 0;
       int found_13 = 0;
   =====
       for (int i = 0; i < length; i++) {
   =====
           if (found_13) {
   =====
               found_13 = 0; }
   =====
           else if (nums[i] == 13) {
   =====
               found_13 = 1; }
   =====
           else {
   =====
               total += nums[i]; }
   =====
       return total;}

.. parsonsprob:: c3dnd-sum13-wd
   :adaptive:
   :numbered: left
   :language: c++

   Create a function ``sum13(nums)`` that takes a list of numbers, ``nums`` and 
   returns the sum of the numbers in the list. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is the empty list. 
   
   .. table:: 
         :name: c3dnd-sum13-wd-table
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
   #include &lt;stdio.h&gt;
   =====
   int sum_13(int* nums, int length) {
   =====
   int sum13(int nums, int size) { #paired: nums should be an array
   ===== 
       int total = 0;
       int found_13 = 0;
   =====
       for (int i = 0; i < length; i++) {
   =====
       for (int i = 0; i <= size; i++) { #paired: should be i < size
   =====
           if (found_13) {
   =====
               found_13 = 0; }
   =====
           else if (nums[i] == 13) {
   =====
           else if (nums[i] = 13) { #paired: Should use equallity opeartor == not assignment operator =
   =====
               found_13 = 1; }
   =====
           else {
   =====
               total += nums[i]; }
   =====
       return total;}

.. parsonsprob:: c3dnd-front-back-nd
   :numbered: left
   :adaptive:
   :language: c++

   Create the function ``frontBack(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.
   For this problem you can assume that that string.h has been included.
  
   .. table:: 
      :name: c3dnd-front-back-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``frontBack("Opening time", "Open", "noon")``      | ``"s"``         |
      +----------------------------------------------------+-----------------+
      | ``frontBack("Afternoon", "Open", "noon")``         | ``"e"``         |
      +----------------------------------------------------+-----------------+
      | ``frontBack("Open at noon", "Open", "noon")``      | ``"s_e"``       |
      +----------------------------------------------------+-----------------+
      | ``frontBack("Closed", "Open", "noon")``            | ``"n"``         |
      +----------------------------------------------------+-----------------+
      | ``frontBack("It is noon now", "open", "noon")``    | ``"n"``         |
      +----------------------------------------------------+-----------------+

   -----
   #include &lt;stdio.h&gt;
   #include &lt;string.h&gt;
   =====
   char* front_back(char* str, char* start, char* end) {
   =====
       int last = -1 * strlen(end);
   =====
       if (strncmp(str, start, strlen(start)) == 0 && strcmp(str + last, end) == 0) {
   =====
           return "s_e"; }
   =====
       else if (strncmp(str, start, strlen(start)) == 0) {
   =====
           return "s"; }
   =====
       else if (strcmp(str + last, end) == 0) {
   =====
           return "e"; }
   =====
       return "n"; }

.. parsonsprob:: c3dnd-front-back-wd
   :numbered: left
   :adaptive:
   :language: c++

   Create the function ``front_back(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.
  
   .. table:: 
      :name: c3dnd-front-back-wd-table
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
   #include &lt;stdio.h&gt;
   #include &lt;string.h&gt;
   =====
   char* front_back(char* str, char* start, char* end) {
   =====
   char frontBack(char* str, char* start, char* end) { #paired: return type should be char* as a string is being returned
   =====
       int last = -1 * strlen(end);
   =====
       int last = strlen(end); #paired: last should be negative as it is used to index from the end of the string
   =====
       if (strncmp(str, start, strlen(start)) == 0 && strcmp(str + last, end) == 0) {
   =====
           return "s_e"; }
   =====
       else if (strncmp(str, start, strlen(start)) == 0) {
   =====
           return "s"; }
   =====
       else if (strcmp(str + last, end) == 0) {
   =====
       else if (strcmp(str, end) == 0) { #paired: should be comparing the end of the string and, as such, should add last 
   =====
           return "e"; }
   =====
       return "n"; }


.. parsonsprob:: c3dnd-bob-there-nd
   :numbered: left
   :adaptive:
   :language: c++

   Create a function, ``bobThere(str)`` that takes a string, ``str``. It
   returns ``True`` if ``str`` contains a "bob" string, but where the middle
   'o' char can be any char. Otherwise it returns ``False``.

   .. table:: 
      :name: c3dnd-bob-there-nd-table
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
   #include &lg;stdio.h&gt;
   #include &lg;string.h&gt;
   =====
   int bobThere(char* str) {
   =====
       int length = strlen(str);
   =====
       for (int i = 0; i < length - 2; i++) {
   =====
           if (str[i] == 'b' && str[i + 2] == 'b') {
   =====
               return 1;}
   =====
       return 0;}

.. parsonsprob:: c3dnd-bob-there-wd
   :numbered: left
   :adaptive:
   :language: c++

   Create a function, ``bobThere(str)`` that takes a string, ``str``. It returns ``True`` if ``str`` contains 
   a "bob" string, but where the
   middle 'o' char can be any char. Otherwise it returns ``False``.

   .. table:: 
      :name: c3dnd-bob-there-wd-table
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
   #include &lg;stdio.h&gt;
   #include &lg;string.h&gt;
   =====
   int bobThere(char* str) {
   =====
   bobThere(char* str) { #paired: return type should be bool
   =====
       int length = strlen(str);
   =====
       for (int i = 0; i < length - 2; i++) {
   =====
       for (int i = 0; i < string_length(str) - 2; i++) { #paired: need to iterate over the length minus 2 so as not to go out of bounds
   =====
           if (str[i] == 'b' && str[i + 2] == 'b') {
   =====
           if (str[i] == 'b' && str[i] == 'b') { #paired: Needs to check if the first and last letter are b
   =====
               return 1;}
   =====
       return 0;}

.. parsonsprob:: c3dnd-palindrome-number-nd
   :numbered: left
   :adaptive:

   Create a function ``int isPalindrome(char* x)`` that takes a string, ``x``, and returns
   ``1`` if x is a palindrome , and ``0`` otherwise.   A string is a palindrome
   if the characters read the same backwards as forwards.

   .. table::
      :name: c3dnd-palindrome-number-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+------------------------------------+
      | Example Input                    | Expected Output                    |
      +==================================+====================================+
      |``isPalindrome("121")``           | ``1``                              |
      +----------------------------------+------------------------------------+
      |``isPalindrome("888")``           | ``1``                              |
      +----------------------------------+------------------------------------+
      |``isPalindrome("678")``           | ``0``                              |
      +----------------------------------+------------------------------------+
   -----
   int isPalindrome(char* x) {
   =====
      int left = 0;
      int right = strlen(x) - 1;
   =====
      while (left < right) {
   =====
         if (x[left] != x[right]) {
   =====
              return 0;}
   =====
        left ++;
        right --;}
   =====
      return 1;}



.. parsonsprob:: c3dnd-palindrome-number-wd
   :numbered: left
   :adaptive:
   :language: c++

   Create a function ``int isPalindrome(char* x)`` that takes a string, ``x``, and returns
   ``1`` if x is a palindrome , and ``0`` otherwise.   A string is a palindrome
   if the characters read the same backwards as forwards.

   .. table::
      :name: c3dnd-palindrome-number-wd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+------------------------------------+
      | Example Input                    | Expected Output                    |
      +==================================+====================================+
      |``isPalindrome("121")``           | ``1``                              |
      +----------------------------------+------------------------------------+
      |``isPalindrome("888")``           | ``1``                              |
      +----------------------------------+------------------------------------+
      |``isPalindrome("678")``           | ``0``                              |
      +----------------------------------+------------------------------------+
   -----
   int isPalindrome(char* x) {
   =====
   int isPalindrome(char x) { #paired: need to pass in a string, not a char
   =====
      int left = 0;
      int right = strlen(x) - 1;
   =====
      while (left < right) {
   =====
      while (left > right) { #paired: need to check if left is less than right
   =====
         if (x[left] != x[right]) {
   =====
         if (x[left] == x[right]) { #paired: need to check if the left and right characters are the same
   =====
              return 0;}
   =====
        left ++;
        right --;}
   =====
      return 1;}
