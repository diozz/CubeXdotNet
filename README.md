# Overview

CubeX is an implementation of the famous [Fridrich Method (or CFOP Method)](https://en.wikipedia.org/wiki/CFOP_Method) in C#. It can generate layer-by-layer solutions to any valid scramble of a 3x3x3 Rubik's Cube, with an average of around 63 moves. Only cubes with standard color scheme [with opposite colors as Yellow-White, Green-Blue and Red-Orange] are currently supported.

# Basics

`FridrichSolver` class can be used to create an instance of solver. It takes a string that represents a scrambled cube. The string can contain characters 'g','o','b','r','y' or 'w' ; Each denoting colors Green, Orange, Blue, Red, Yellow and White respectively. The string therefore, should contain exactly 54 characters (9 Cubelets * 6 Faces) that represents the cube state. The order in which the color is to be entered is:

![](https://i.imgur.com/pR2Zkia.png)

For example a solved cube is represented by : `"gggggggggooooooooobbbbbbbbbrrrrrrrrryyyyyyyyywwwwwwwww"`

# Quickstart

 ```c#
 FridrichSolver Solver = new FridrichSolver("gygrgogwgoyogobowobybobrbwbryrbrgrwryoybygyrywrwbwgwow"); //The Superflip!

 Solver.Solve();

 if(Solver.IsSolved)
 {
     Console.WriteLine("Solution ({0} Moves) : {1}", Solver.Length, Solver.Solution);
 }
 ```

Go through the provided sample for better understanding.

![](https://i.imgur.com/VlMntOB.png)

# Want more?

Check out CubeX, a feature pumped Rubik's Cube Solver for Android, powered by this library.
[![Get it on Google Play](https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png)](https://play.google.com/store/apps/details?id=diozz.cubex)

# License

See the [LICENSE](https://github.com/diozz/CubeXdotNet-Rubiks-Cube-Solver/blob/master/LICENSE) file for license rights and limitations.

