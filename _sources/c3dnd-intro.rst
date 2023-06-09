Introduction to Problem Types
-----------------------------------------------------

Please read the following, watch the videos, and try to solve the problems.


Solving Mixed-up Code Problems
==================================

If you see a problem like the one below you will need to put the mixed-up
code in the correct order on the right side. You
may need to indent the blocks as well.  There may also be extra blocks that are not
needed in a correct solution that you can leave on the left side. Click the "Check" button
to check your solution.

See the video below for an example.

.. youtube:: Rf7oWHlo-e0
    :divid: iwgex1-parsons1-c3dnd
    :optional:
    :width: 650
    :height: 415
    :align: center

Try to solve the following mixed-up code problem.  This problem doesn't require any indentation.

.. parsonsprob:: intro-simple-parsons-no-indent-c3dnd
   :numbered: left
   :adaptive:
   :practice: T
   :order: 3, 1, 2, 0

   Drag the blocks from the left and put them in the correct order on the right. The text in each block
   defines the order.
   -----
   First block
   =====
   Second block
   =====
   Third block

Try to solve the following mixed-up code problem. This problem requires indentation.

.. parsonsprob:: intro-simple-parsons-indent-c3dnd
   :numbered: left
   :adaptive:
   :practice: T
   :order: 3, 1, 2, 0

   Drag the blocks from the left and put them in the correct order on the right with the correct indentation.
   The text in each block defines the order and indentation.
   -----
   First block
   =====
   Second block
   =====
       Third block that needs to be indented

Try to solve the following mixed-up code problem. This problem requires indentation and has extra blocks that are not needed in a correct solution.

.. parsonsprob:: intro-simple-parsons-indent-with-dist-c3dnd
   :numbered: left
   :adaptive:
   :practice: T
   :order: 3, 1, 2, 0

   Drag the blocks from the left and put them in the correct order on the right with the correct indentation.
   There is an extra block that is not needed in the correct solution.
   -----
   First block
   =====
   Second block
   =====
   Extra block that is not needed #paired: This block is not needed
   =====
       Third block that needs to be indented

The mixed-up code problems have a "Help me" button at the bottom of the
problem. Once you have checked at least three incorrect solutions you can
click the button for help.  It will remove an incorrect code block, if you used
one in your solution, or combine two blocks into one if there are more
than three blocks left.

See the video below for an example.

.. youtube:: QejZ7u642IU
    :divid: iwgex1-parsons2-c3dnd
    :optional:
    :width: 650
    :height: 415
    :align: center

Solving Write Code Problems
==============================

If you see a problem like the one below, you will need to write code.  The problem
will have unit tests that you can run to check that your code is working
correctly.  Click on the "Run" button to compile and run your code.  Look after
the code area for compiler errors and/or unit test results.

See the video below for an example.

.. youtube:: w9hTOJ7iJpE
    :divid: c3dnd-write-code-video-ex
    :optional:
    :width: 1020
    :height: 826
    :align: center

Finish writing the code for the following problem.

.. activecode:: intro-sample-write-code-triple-ps
    :language: c

    Write a function called ``triple(int num)`` that takes a number ``num`` and
    returns the number times 3. For example, ``triple(2)`` should return 6 and
    ``triple(-1)`` should return -3. 
    ~~~~
    #include<stdio.h>

    int triple(int num) {
        // write code here    
    }

    int main() {
        printf("%d\n", triple(2));
        printf("%d\n",triple(-1));

        return 0;
    }

Feedback
==================================

.. shortanswer:: c3dnd-intro-sa

   Please provide feedback here. Please share any comments, problems, or suggestions.


What to do next
============================

.. raw:: html

    <p>Click on the following link to go the practice problems: <a id="c3dnd-practice"><font size="+2">Practice Problems</font></a></p>


.. raw:: html

   <script type="text/javascript">

     function getCookie(cname) {
        let name = cname + "=";
        let decodedCookie = decodeURIComponent(document.cookie);
        let ca = decodedCookie.split(';');
        for(let i = 0; i <ca.length; i++) {
           let c = ca[i];
           while (c.charAt(0) == ' ') {
              c = c.substring(1);
           }
           if (c.indexOf(name) == 0) {
              return c.substring(name.length, c.length);
           }
        }
        return "";
     }

     function setCookie(cname, cvalue) {
        document.cookie = cname + "=" + cvalue + ";";
     }

     window.onload = function() {

        a = document.getElementById("c3dnd-practice")

        // get prev set cookie
        var EXP_COOKIE = 'c3dnd'
        var cond = getCookie(EXP_COOKIE);

        // if no prev set cookie: generate random condition and set cookie
        if (cond != 'd' && cond != 'nd') {
           var v = Math.floor(Math.random() * 2);
           if (v < 1) {
               cond = 'd';
           } else {
               cond = 'nd';
           }
           setCookie(EXP_COOKIE, cond);
        }

        if (cond == 'd') {
           a.href = "c3dnd-pwd.html"
        } else if (cond == 'nd') {
           a.href = "c3dnd-pnd.html"
        }
     };
   </script>
