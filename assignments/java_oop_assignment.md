[Back](../readme.md)

# Object Oriented Programming Assignment
In this assignment, you will put your OOP skills to test. In this assignment, you will be creating a fake robot.

## Instructions

1.	Create a new java project. If you have an IDE (such as intellij, eclipse or netbeans) on your computer use that. Otherwise, use [this online Java IDE](https://www.jdoodle.com/online-java-compiler-ide/). If you need help using the ide, talk to the code team lead.
2.	Create a class called Robot. In this class should be your main method
3.	Create another class called Motor.
    *	The constructor should take in an integer for the motor id.
    *	This class should have a method called `setSpeed()`, and should take in a speed as a double. The function should print out the following to the console: 
    <br>`motor [number] speed set to [speed]`<br> where *speed* is the speed passed in and *number* is the motor id.
4.	In your main method, 2 motors. One should be for the left of the robot, and the other should be the right of the robot.
5.	Create a class called Controller.
    * The class should have a method called `takeInput()`. This function should loop and take in user input (hint: use the `java.util.Scanner` class). Pass in any required variables into the function to make it work.
        * If the person enters forward, set the left and right motors to have a positive speed.
        * If the person enters backward, set the left and right motors to have a negative speed.
        * If the person enters left, set the left motor to have a negative speed and the right motor to have a positive speed.
        * If the person enters right, set the right motor to have a positive speed and the left motor to have a negative speed.
        * If the person enters stop, set the motor speeds to be off and stop the program.
6.	Create a Controller in the main method.
7.	Call ``controller.takeInput()``
8.	Test your code and make sure the correct lines are printed to the console.
### Bonus
Design wise, it is not the best idea to have the controller have direct control over the motors. Logically, it doesn’t make sense for the controller to be tied to the motors on the robot. The controller class should just take in input and tell something else to set the motor speeds. Find a way to set the motor speed without making the controller aware of the motors (this means no passing in the motors to the function, and no passing the motors into the constructor). Keep any logic outside the main Robot class.
