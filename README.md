# Optimus Path

Optimus Path is a Python class designed to find a path in a grid-based environment while considering certain priority rules and special symbols.

## Features

- **Direction Enumeration:** The class utilizes an enum called `Direction` to represent cardinal directions: SOUTH, EAST, NORTH, and WEST.
- **Priority Enumeration:** Another enum named `Priority` defines two priority sequences for directions: SOUTHEASTNORTHWEST and WESTNORTHEASTSOUTH.
- **Special Symbols:** Special symbols such as 'I' (INVERT) and 'B' (BREAKMODE) are represented using the `SpecialSymbol` enum to indicate special functionalities.
- **Path Finding Algorithm:** The `OptimusPath` class employs a path-finding algorithm to traverse the grid, considering priority rules and handling special symbols along the way.
- **Teleportation Support:** The class supports teleportation within the grid, enabling movement between teleportation points.

## Usage

1. **Initialization:** Instantiate the `OptimusPath` class by providing the height (`H`), width (`W`), and grid (`grid`) of the environment.
2. **Finding Path:** Call the `findPath()` method to execute the path-finding algorithm and determine the optimal path from the start to the end point.
3. **Special Symbols Handling:** The algorithm handles special symbols 'I' and 'B' to manage invert mode and break mode, respectively.
4. **Printing Output:** The `printOutput()` method prints the final path discovered by the algorithm.

## Example

```python
# Example usage of OptimusPath class
optimus = OptimusPath(H, W, grid)
optimus.findPath()

## Dependencies

- **collections:** This module is used for working with collections of data in Python.
- **enum:** This module provides support for enumerations in Python.

## Credits

- This project is maintained by Sumedha Khatter as a part of Tesla Coding Challenge.


