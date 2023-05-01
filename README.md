Download Link: https://assignmentchef.com/product/solved-bits-and-pieces-part-2-electric-boogaloo
<br>
<strong><u>Background</u></strong>: All numbers (both integer and float types) that are used in any computer program are always stored in memory (typically RAM) as binary numbers. The range of possible values for these numbers is dependent on how the computer hardware has been constructed (fun fact: the area of research whose focus is on the design and implementation of a set of rules and methods describing the functionality, organization, and implementation of computers is known as computer architecture), and most modern computers have either 32-bit or 64-bit architectures. However, most computing systems (about 98% of microprocessors that are manufactured) are embedded systems, which performs a dedicated function within a larger system. For example, many household appliances such as microwaves and washing machines make use of embedded systems in performing their functions. An important characteristic of embedded systems is that their architectures are much smaller and can typically be 8-bit or 16bit. To be able to work in such an environment, bitwise operators are utilized in all aspects of embedded systems programming to configure specific registers in performing a specified function.




In this assignment, an 8-bit architecture will be “simulated” in the sense that the values to be passed in the required functions will only be in the range of [0, 255]. Note that the number of possible values that this range contains is exactly 2<sup>8</sup> = 256.




<table width="623">

 <tbody>

  <tr>

   <td width="78">BIT7</td>

   <td width="78">BIT6</td>

   <td width="78">BIT5</td>

   <td width="78">BIT4</td>

   <td width="78">BIT3</td>

   <td width="78">BIT2</td>

   <td width="78">BIT1</td>

   <td width="78">BIT0</td>

  </tr>

 </tbody>

</table>




The above is representative of how an 8-bit register may appear, with BIT7 being known as the most-significant-bit (<strong>MSB</strong>), and BIT0 being known as the least-significant-bit (<strong>LSB</strong>).




In regard to bitwise operators, and within the context of embedded systems programming, one can manipulate the values of each register by either setting or clearing bits. Setting a bit means that a specific bit value in a register will be changed to a <strong>1 </strong>without altering the values of the other bits, regardless of the current value of the register. For example, if BIT4 is to be set in a register, then this can be accomplished by doing the following: register = register | BIT4.




To clear a bit means that a specific bit value in a register will be changed to a <strong>0 </strong>without altering the values of the other bits, regardless of the current value of the register. For example, if BIT4 is to be cleared in a register, you will first have to negate the bit to turn it into a <strong>0</strong> while changing all other bits in the value to <strong>1</strong>, then do a bitwise and operation. To clarify, the binary representation of BIT4 is 0001 0000. Negating BIT4, i.e. ~BIT4, will return 1110 1111. To complete the explanation, the following is done to accomplish clearing a bit: register = register &amp; (~BIT4).

<strong> </strong>

<strong><u>Objective</u></strong>: The purpose of this assignment is to provide background into embedded systems programming, obtain some familiarity with bitwise operators, and to get back into a programming shape. All of the required functions are not meant to tricky and are the most straight-forward I have ever created.




Thorough explanations were provided in the concepts of setting and clearing a bit. Please ponder for a moment on how to accomplish a bit extraction (i.e. you want to obtain the value of a specific bit in a register) and how to check for the status of a bit, as described in the <strong>Required Functions</strong> section of the assignment.




<h2>Required Functions</h2>




<h3>            bit_status(num, bit)</h3>

<em>                         </em>

<em>                        </em><strong>Description</strong>: Determine if the passed <em>bit</em> is present in the passed number. In                     other words




<strong>Output</strong>: This function should not print anything onto the screen.




<strong>Return Value</strong>: Return <strong>True</strong> if the specified bit is set. In other words, the value of the bit is 1. Return <strong>False</strong> otherwise.







<h3>set_bit(num, bit)</h3>

<em> </em>

<strong>Description</strong>: Set the specified <em>bit</em> into the passed number <em>num</em>. In other words, have the bit value be a 1.




<strong>Output</strong>: This function should not print anything onto the screen.




<strong>Return Value</strong>: A value with the set bit.







<h3>            clear_bit(num, bit)</h3>




<strong>Description</strong>: Clear the specified <em>bit</em> from the passed number <em>num</em>. In other words, have the bit value be a 0.




<strong>Output</strong>: This function should not print anything onto the screen.




<strong>Return Value</strong>: A value with the cleared bit.




<h3>extract_bit(num, bit)</h3>

<em> </em>

<strong>Description</strong>: Obtain the specified bit value of the passed number <em>num</em>.




<strong>Output</strong>: This function should not print anything onto the screen.




<strong>Return Value:</strong> A value representing the extracted bit.







<h2>Testing</h2>




Total tests: 32




Testing will be done using the <strong>bits_and_pieces_part2_tester.py </strong>




<strong>NOTE</strong> – The <em>bit_status()</em> function is used in the testing of the <em>set_bit()</em> and <em>clear_bit()</em>  functions to determine if the bit was successfully set and/or cleared.




<h2> Notes</h2>




Name your program “bits_and_pieces.py”, otherwise the program tester will NOT work.




If you have any questions on this assignment, or encounter an issue or bug that you are  not able to isolate and figure out on your own AFTER consulting with your peers, please email me at <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="53373a3229347d3426202732253c3213383d3a343b27207d2630357d3637267d">[email protected]</a>