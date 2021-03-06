# STRUCTURES-NI-LABVIEW
Explanation about different structures in NI LABVIEW
FOR LOOP: Executes its subdiagram n times, where n is the value wired to the count (N) terminal. The iteration (i) terminal provides the current loop iteration count, which ranges from 0 to n-1.

WHILE LOOP: Repeats the code within its subdiagram until a specific condition occurs. A While Loop always executes at least one time,where iteration (i) terminal provides the current loop iteration count, which ranges from 0 to n-1 and a condition terminal which may be  either stop if true or continue if true.

CASE STRUCTURE: Contains one or more subdiagrams, or cases, exactly one of which executes when the structure executes. The value wired to the selector terminal determines which case to execute.It contains, 1)Case selector label which displays the value(s) for which the associated case executes.2)Subdiagram contains the code that executes when the value wired to the case selector terminal matches the value that appears in the case selector label.3)Selector terminal which selects which case to execute based on the value of the input data. The input data can be a Boolean, string, integer, enumerated type.

FORMULA NODE: Evaluates mathematical formulas and expressions similar to C on the block diagram. The following built-in functions are allowed in formulas: abs, acos, acosh, asin, asinh, atan, atan2, atanh, ceil, cos, cosh, cot, csc, exp, expm1, floor, getexp, getman, int, intrz, ln, lnp1, log, log2, max, min, mod, pow, rand, rem, sec, sign, sin, sinc, sinh, sizeOfDim, sqrt, tan, tanh.

FLAT SEQUENCE: Consists of one or more subdiagrams, or frames, that execute sequentially. Use the Flat Sequence structure to ensure that a subdiagram executes before or after another subdiagram.Data flow for the Flat Sequence structure differs from data flow for other structures. Frames in a Flat Sequence structure execute from left to right and when all data values wired to a frame are available. The data leaves each frame as the frame finishes executing. This means the input of one frame can depend on the output of another frame.

I have used a for loop and a while loop enclosed within a case structure.Also i have used a formula node with a simple expression.Now this case structure and formula node is enclosed in a flat sequence.

[loop 1 bd.zip](https://github.com/RajeshSubbu/STRUCTURES-NI-LABVIEW/files/1036366/loop.1.bd.zip)

[LOOP fp.zip](https://github.com/RajeshSubbu/STRUCTURES-NI-LABVIEW/files/1036370/LOOP.fp.zip)

In this video,true case is executed in case structure by switching ON the horizontal toggle switch,where i have used  a for loop.Therefore the execution is finished after n cycles.

[loop 1f bd.zip](https://github.com/RajeshSubbu/STRUCTURES-NI-LABVIEW/files/1036393/loop.1f.bd.zip)

[loop 1f fp.zip](https://github.com/RajeshSubbu/STRUCTURES-NI-LABVIEW/files/1036395/loop.1f.fp.zip)

In this video,false case is executed in case structure by switching OFF the horizontal toggle switch,where i have used a while loop.Therefore the loop runs continuosly till i press the stop button in front panel.

TIMED LOOP: Executes one or more subdiagrams, or frames, sequentially each iteration of the loop at the period you specify. Use the Timed Loop when you want to develop VIs with multirate timing capabilities, precise timing, feedback on loop execution, timing characteristics that change dynamically, or several levels of execution priority. Right-click the structure border to add, delete, insert, and merge frames.

Here in this example i have used 2 timed loops,one with small delay for iteration and another with large delay for iteration.

[structure.vi Front Panel _ 5_29_2017 11_30_35 PM.zip](https://github.com/RajeshSubbu/STRUCTURES-NI-LABVIEW/files/1036412/structure.vi.Front.Panel._.5_29_2017.11_30_35.PM.zip)

EVENT STRUCTURE: Waits until an event occurs, then executes the appropriate case to handle that event. The Event structure has one or more subdiagrams, or event cases, exactly one of which executes when the structure executes to handle an event. This structure can time out while waiting for notification of an event. Wire a value to the Timeout terminal at the top left of the Event structure to specify the number of milliseconds the Event structure waits for an event. The default is -1, which indicates never to time out.

Here in this example i have used 2 frames such as mouse enter,mouse leave.When the mouse pointer enters the front panel,the LED light glows.When the mouse pointer leaves the front panel,the LED will be turned off.

[event structure.vi Front Panel 5_30_2017 12_06_46 AM.zip](https://github.com/RajeshSubbu/STRUCTURES-NI-LABVIEW/files/1036452/event.structure.vi.Front.Panel.5_30_2017.12_06_46.AM.zip)
