#Robot Simulator Code Challenge

##Description:

The application is the simulation of a robot moving on a grid tabletop. Dimensions are 10 x 10 units.
There are no obstructions on the table's surface, and the robot is free to roam around the surface of the table, but must be prevented from falling off the edges.

Any movement that would result in the robot falling off the edges must be prevented, however further valid movement commands must still be allowed.

Create an application that can read an input file containing a list of commands:

DROP X,Y,D
MOVE
LEFT
RIGHT
REPORT

DROP will put the robot on the table in at the X & Y coordinates, facing either NORTH, SOUTH, EAST or WEST.
The coordinates (0,0) can be considered to be the SOUTH WEST most corner.

The first valid command to the robot is the DROP command, after that, any sequence of commands may be issued, in any order, including another DROP command. The application should discard all commands in the sequence until a valid PLACE command has been executed.

MOVE will move the robot one unit forward in the direction that it is currently facing.

LEFT and RIGHT will rotate the robot 90 degrees in the specified direction.

REPORT will announce the X, Y and D of the robot. This can just be a simple console output.

##Constraints: 
The robot must not fall off the table during movement. This also includes the initial placement of the toy robot. Any move that would cause the robot to fall must be ignored.

Example Input and Output:

a) DROP 0,0,NORTH MOVE REPORT Output: 0,1,NORTH

b) DROP 0,0,NORTH LEFT REPORT Output: 0,0,WEST

c) DROP 1,2,EAST MOVE MOVE LEFT MOVE REPORT Output: 3,3,NORTH

Deliverables: The JavaScript (Node JS) source files, the test data and any test code.
It is not required to provide any graphical output showing the movement of the toy robot.

Please submit your completed products as a pull request to this repository.
