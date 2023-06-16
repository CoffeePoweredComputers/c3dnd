Post Test
-----------------------------------------------------

Please answer
the following problems to the best of your ability without any
outside help. You can stop working on a problem after you worked
on it for about five minutes without solving it.

Problems
==============

.. activecode:: c3dnd-upper-center
   :language: c

   Write the function ``char* upper_center(char* str)`` to return the passed string ``str`` with the middle character(s) in uppercase.

   * If ``str`` has an odd length, uppercase the middle character.
   * If ``str`` has an even length, uppercase the middle two characters.
   * If ``str`` has less than 3 characters then return ``str``.

   .. table::
      :name: c3dnd_upper_center-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``upper_center('abc')``           | ``'aBc'``                             |
      +----------------------------------+---------------------------------------+
      |``upper_center('abcd')``          | ``'aBCd'``                            |
      +----------------------------------+---------------------------------------+
      |``upper_center('a')``             | ``'a'``                               |
      +----------------------------------+---------------------------------------+
   ~~~~
   #include <stdio.h>
   #include <string.h>

   char* upper_center(char* str){
      // TODO
   }

.. activecode:: c3dnd-post-is-descending
   :language: c

    Write a function ``int is_descending(int* nums)`` to do the following.

    * Return ``1`` if the  numbers in the list ``nums`` are sorted in descending order.
    * Otherwise return ``0``.
    * If the list ``nums`` has less than two numbers in it return ``1``.

    .. table::
       :name: p3dnd_is_ascending_ac-table
       :class: longtable
       :align: left
       :width: 80%

        +----------------------------------+------------------------------------+
        | Example Input                    | Expected Output                    |
        +==================================+====================================+
        |``is_descending({2,3,4})``        | ``0``                              |
        +----------------------------------+------------------------------------+
        |``is_descending({1})``            | ``1``                              |
        +----------------------------------+------------------------------------+
        |``is_descending({4,3,2})``        | ``1``                              |
        +----------------------------------+------------------------------------+
   
   ~~~~
   int is_descending(int* nums){
      // TODO
   }

.. activecode:: c3dnd-post-sum67
   :language: c

   Write the function ``int sum67(int* nums)`` that takes a list of numbers and
   returns the total of the numbers in the list except for all the
   numbers whose position is between a 6 and 7 in the list (inclusive).

   .. table::
      :name: p3dnd_sum67_fix_table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``sum67({1,2})``                  | ``3``                                 |
      +----------------------------------+---------------------------------------+
      |``sum67({2, 6, 8, 7, 2})``        | ``4``                                 |
      +----------------------------------+---------------------------------------+
      |``sum67({3, 6, 7})``              | ``3``                                 |
      +----------------------------------+---------------------------------------+
   ~~~~
   int sum67(int* nums)``{
      // TODO
   }

.. activecode:: c3dnd-post-almost-palindrome
   :language: c

   Write the function ``int isAlmostPalindrome(char* x)`` that takes a string, ``x``, and returns
   ``1`` if x can be a palindrome after deleting at most one character from it,
   and ``0`` otherwise.   A string is a palindrome if the characters read the
   same backwards as forwards.

   .. table::
      :name: c3dnd-post-almost-palindrome-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+------------------------------------+
      | Example Input                    | Expected Output                    |
      +==================================+====================================+
      |``isAlmostPalindrome("aba")``     | ``1``                              |
      +----------------------------------+------------------------------------+
      |``isAlmostPalindrome("abca")``    | ``1``                              |
      +----------------------------------+------------------------------------+
      |``isAlmostPalindrome("abc")``     | ``0``                              |
      +----------------------------------+------------------------------------+
   ~~~~
   int isAlmostPalindrome(char* x)``{
      // TODO
   }

Feedback
==================================

.. shortanswer:: c3dnd-posttest-sa

   Please provide feedback here. Please share any comments, problems, or suggestions.

What to do next
============================
.. raw:: html

    <p>Click on the following link to go to the post survey: <b><a id="c3dnd-postsurvey"><font size="+2">Post Test</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("c3dnd-postsurvey")
        a.href = "c3dnd-postsurvey.html"
      };

    </script>
