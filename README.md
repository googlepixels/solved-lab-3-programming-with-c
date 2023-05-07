Download Link: https://assignmentchef.com/product/solved-lab-3-programming-with-c
<br>
Lab 3Programming with COverviewYou will design and write a program that asks the user to select a trigonometric function from a menu and you will then calculate and display the value of the selected function for every 15 degrees, starting from 0 degrees up to 90 degrees.

ObjectivesFamiliarize yourself with C math functionsPractice program design and organizationPractice using enum and typedef – More InfoPractice using a switch constructMore practice with loops, ifs, and a user input menu.RequirementsYou should attempt to organize your code in a clean and logical manner. Do not place all of your code in your main function, but rather divide your program goal into subtasks and create a function for each of these subtasks.You will display your user menu as part of a user controlled loop.

Please choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice

Each time you display the menu you will read in the user’s response, process their request, display the results, and repeat the menu again. Your loop will terminate only once the user has selected the last option (QUIT). You may assume the user will only enter an integer. Do not change the order or numbering of this menu.If a user selects an invalid option to the menu (e.g. 4), you should display an error and repeat the menu again. For example:

4 is an invalid option. Please try again.

Observe that the error message should repeat back the option the user selected.You are to use an enum named MENU as part of your command-line interface options. Specifically, you should create an enum for the four choices (Sine, Cosine, Tangent, QUIT). You should wrap this enum with a type definition, named menu_t (menu type).Every time the user enters a value, you will use a switch statement to compare against each case of your enum. The numbers 0, 1, 2, 3 should not appear in your user menu control as you must use your user-defined enum. You will also refer to your enum value QUIT in your user controlled menu loop, rather than 3.

TIP: Because all enums are stored internally as unsigned integers, you should use the “%u” formatting code to read in the user input in your scanf statement, but you will store the value the user entered in a variable of type menu_t.You are required to use two constants in your program:

PI is 3.14159LOOP_LIMIT is 90 These constants must be defined near the top of your program. Refer to these constants throughout your program and not the values directly.NOTE: You may lose points if you retype these values throughout your program.

TIP: Because you are using a constant to define the LOOP_LIMIT, we should be able to easily change your program to print out up to 360 degrees by only changing one value at the top of your program.Format your results showing four places after the decimal point, as shown in the Example Execution. Achieve the indentation using a TAB in your printf function

TIP: The control character for TAB is “t”.To display the trigonometric results, you will use a for loop based on degrees, starting from zero and counting up to LOOP_LIMIT by step of 15 degrees.The trigonometric functions you will use takes in a value in radians. Therefore you must convert each degree value to radians before passing to the trigonometric function. The relationship between degrees and radians is:

r=π⋅d180r=π⋅d180

where rr is radians and dd is degrees. If you fail to convert degrees to radians, you will produce incorrect values.

NOTE: To use the sin, cos and tan functions, you will need to import the math.h library.tan(90.0) is an infinite number. You must explicitly look for and handle the case of tan(90.0) and you must print UNDEFINED instead. If you do not, you will display an incorrect value and may lose points.Example Execution[esus] $ ./program3Please choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice 44 is an invalid option. Please try again.Please choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice -1-1 is an invalid option. Please try again.Please choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice 0sin(0) = 0.0000sin(15) = 0.2588sin(30) = 0.5000sin(45) = 0.7071sin(60) = 0.8660sin(75) = 0.9659sin(90) = 1.0000Please choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice 1cos(0) = 1.0000cos(15) = 0.9659cos(30) = 0.8660cos(45) = 0.7071cos(60) = 0.5000cos(75) = 0.2588cos(90) = 0.0000Please choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice 2tan(0) = 0.0000tan(15) = 0.2679tan(30) = 0.5773tan(45) = 1.0000tan(60) = 1.7320tan(75) = 3.7320tan(90) is UNDEFINEDPlease choose an option: (0) Sine (1) Cosine (2) Tangent (3) QUITEnter your choice 3You chose QUIT. Thank you, come again!

CompileCompile your program using this gcc command:

$ gcc -std=c99 -Wall -lm lab3.c -o program3

The additional -lm flag is required because we are using the math library.

TestTest your program! There are a number of choices you may make during your design and implementation. Make sure you test each one of your trigonometric functions, your QUIT condition, and any input integers that are out of bounds of the menu options.

NOTE: Make sure you output what is expected, nothing more and nothing less. Do not change the order or the number associated with each of the menu options, otherwise the grading script will choose incorrectly.

Try to recreate the output of the Example Execution by making the same menu choices given in the example. Does your output look the same?ResourcesYou should attend the Friday Lab session to seek assistance from the TAs and CAs.For general questions, check the D2L Lab 3 Help Forum to see if another student has already asked your question. Otherwise, post your question on the D2L forum. This forum is intended for general questions that will benefit all students. Do not paste your code nor give away any specific answers to the lab on this forum.For specific questions, attend the weekly lab session or attend the TA’s office hours.You are encouraged to use resources or tutorials on the internet to learn unix or C. Check the class resource list for some links to resources.SubmissionAssigned: February 15thLab Day: February 19thDue Date: February 22nd, 8:00am

Make sure you included ample and informative comments – it is 20% of your grade!Rename your C file to last_first_lab3.c and substitute your last and first name.

NOTE: If you fail to follow the above file naming conventions, your program cannot be graded automatically and you will lose significant points.Submit your .c file to the D2L dropbox Lab 3.

NOTE: Submit only your C file to D2L. Do not submit your object file or executable program. Do not archive (e.g. zip) your file.Each student will complete and submit this assignment individually. Submit your work on or before the deadline as late work will receive a 50% penalty. Labs submitted more than 24 hours late will not be accepted.

5/5 - (1 vote)