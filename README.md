# bp0609-2x2-Rubix-Cube-Solver
 This repository contains a C++ code to solve the 2x2 Rubik's Cube
 The solver utilizes efficient algorithms to find the shortest sequence of moves required to solve any scrambled configuration of the cube.
 - The cube has a total of 8 cubies.
 - Each cubies have 3 distinct colors in them and therefore can have 3 different orentations.
 - There are 8 positions in 2x2 rubix cube and each cubie can be placed amoung these 8 positions.
 - So there are a total of $8! \times 3^8 = 264,539,520$ combinations.
 - Since we need to find shortest moves to solve cube, we will use BFS algorithm.
 - Rules to change configurations of the cube for solving
   1. After giving input of the configuration of the cube, put the cube on a plane surface wihtout moving it.
   2. Now we have 9 pre-defined moves that our program will output. F-Move the front face clockwise 90 deg, U-Move top face clockwise 90 deg, R-Move right face clockwise 90 deg, F1-Front face anticlockwise 90 deg, U1-Top face anticlockwise 90 deg, R1-Right face anticlockwise 90 deg, F2-Front face clockwise 180 deg, U2-Top face clockwise 180 deg, R2-Right face clockwise 180 deg.
   3. After each move the orentation and position of each cubie will change.
   4. We use memoization technique to reduce the computation cost. To do so, we store the current position and orentation of each cubie in an array with some special index encoding so that the mapping does not give an overflow error.
 - Input format of the program
   1. 'RBY','OWR',...... These types of input are required, where R, B, W ... are the color initials of red, blue, white colors and so on.
   2. There are 8 cubie and we need to give input such that it include the orentaions of color.
   3. Each cubie has exactly 3 colors and the order in which the input color are required are "ABC" where A=Top/Bottom, B=Left/Right, C=Up/Down
   4. Sample input = WRB YBO WOG OGY YRB YRG BWO WGR, where WRB is front face top left cubie, YBO is front-top-left, WOG is front-bottom-left, OGY is front-bottom-right, YRB is back-top-left, YRG is back-top-right, BWO is back-bottom-left, WGR is back-bottom-right.
    
       
