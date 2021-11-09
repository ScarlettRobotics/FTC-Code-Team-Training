[Back](./readme.md)
# Motors
The motor controller you use in the code corresponds to the physical motor on the robot.

## PWM Motor Controllers
These motor controllers are connected to the PWM ports on the robo-rio. These Motor controllers can be defined as follows:

### Spark Controllers
```java
SpeedController controller = new Spark(port);
```
### TalonSP Controllers
```java
SpeedController controller = new VictorSP(port);
```

## Can Motor Controllers
The CAN bus is a system that allows us to connect all the motor controllers in series. This is most useful when we run out of PWM ports on the roborio.

An incomplete list of CAN motor controllers is as follows:

### VictorSPX
```java
SpeedController controller = new VictorSPX(port);
```
### TalonSRX
```java
SpeedController controller = new TalonSRX(port);
```

## Pros of the CAN bus
1. Allows for us to connect as many controllers as we want to the robot.

## Cons of the CAN bus
1. If one cable is disconnected, the entire CAN bus goes down.