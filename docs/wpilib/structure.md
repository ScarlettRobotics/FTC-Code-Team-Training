# WPILib Structure
The robot has a predefined structure. There are two main components to your robot - Subsystems and Commands.

## Subsystems
* Subsystems are responsible for holding referances to everything we want to control on the robot.
    * Motor Controllers
    * Solinoids
    ```java
    SpeedController flMotor = new Spark(0);
    SpeedController frMotor = new Spark(1);
    SpeedController blMotor = new Spark(2);
    SpeedController brMotor = new Spark(3);

    SpeedControllerGroup left = new SpeedControllerGroup(flMotor, blMotor);
    SpeedControllerGroup right = new SpeedControllerGroup(frMotor, brMotor);

    DifferentialDrive transmission = new DifferentialDrive(left, right);
    ```
* Subsystems also expose an interface for interacting with these componenets. For example, a drive train subsystem may have a drive() function:
    ```java
    /**
    Drives the robot using tank drive
    @param left The speed to set the left controllers
    @param right The speed to set the right controllers
    */
    public void drive(double left, double right) {
        transmission.tankDrive(left, right);
    }
    ```

## Commands
Commands use subsystems to control the robot. Subsystems define what you __can__ do with the robot. Commands define how you do it.