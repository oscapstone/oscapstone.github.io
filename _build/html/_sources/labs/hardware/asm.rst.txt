======================
The Assembly You Need
======================

Although this course is not about learning assembly language, you still need to write some assembly in bare metal programming.

Here, we provide pieces of assembly code you possibly need.
After copy and paste, you still need to look up the manual to understand how this codes work.


.. important::
  You might still need others to achieve some extra function.
  Please refer to these manual for more information.  
  https://documentation-service.arm.com/static/613a2c38674a052ae36ca307
  https://developer.arm.com/documentation/100076/0100/a64-instruction-set-reference
  https://developer.arm.com/documentation/ddi0487/latest

#####
Lab 0
#####

.. code-block:: c
  
  // enter busy loop
  _start:
    wfe
    b _start

#####
Lab 1
#####

.. code-block:: c

  // set stack pointer and branch to main function.
  2:
  	ldr x0, = _stack_top
  	mov sp, x0
  	bl main
  1:
  	b 1b
