Practice Problems
-----------------------------------------------------

Please answer
the following problems to the best of your ability without any
outside help. You can stop working on a problem after you worked
on it for about five minutes without solving it.

Problems
==============

.. parsonsprob:: c3dnd-front-back-nd
   :numbered: left
   :adaptive:

   Create the function ``char* front_back(char* str, char* start, char* end)`` that takes three strings and returns
   a string based on the following conditions.

   * If ``str`` contains ``start`` at the beginning of the string return ``"s"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * If ``str`` contains ``start`` at the begining and ``end`` at the end then return  ``"s_e"``.
   * Otherwise return ``"n"``.

   .. table::
      :name: c3dnd-front-back-nd-table
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
   #include <stdio.h>
   #include <string.h>
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

.. parsonsprob:: c3dnd-sum13-nd
   :adaptive:
   :numbered: left

   Create a function ``int sum_13(int* nums, int length)`` that takes a list of
   numbers, ``nums``, and the length of the list, ``length`` and
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
          | ``sum13({13,1,2}, 3)``                             | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({1,13}, 2)``                               | ``1``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({4, 13, 8}, 3)``                           | ``4``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({13, 1, 13, 3, 2}, 4)``                    | ``2``           |
          +----------------------------------------------------+-----------------+
   -----
   #include <stdio.h>
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

.. parsonsprob:: p3dnd-bob-there-nd
   :numbered: left
   :adaptive:

   Create a function, ``int bobThere(char* str)`` that takes a string, ``str``. It returns ``1`` if ``str`` contains
   a "bob" string, but where the
   middle 'o' char can be any char. Otherwise it returns ``0``.

   .. table::
      :name: p3dnd-bob-there-nd-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+------------------------------------+
      | Example Input                    | Expected Output                    |
      +==================================+====================================+
      |``bobThere("abcbob")``            | ``1``                              |
      +----------------------------------+------------------------------------+
      |``bobThere("b9b")``               | ``1``                              |
      +----------------------------------+------------------------------------+
      |``bobThere("bac")``               | ``0``                              |
      +----------------------------------+------------------------------------+
   -----
   #include <stdio.h>
   #include <string.h>
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

Feedback
==================================

.. shortanswer:: c3dnd-nd-parsons-sa

   Please provide feedback here. Please share any comments, problems, or suggestions.

What to do next
============================
.. raw:: html

    <p>Click on the following link to go to the post test: <b><a id="c3dnd-post"><font size="+2">Post Test</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("c3dnd-post")
        a.href = "c3dnd-post.html"
      };

    </script>
