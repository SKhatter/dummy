

# Optimus Path

Optimus Path is a Python class designed to find a path in a grid-based environment while considering certain priority rules and special symbols.

## Features


- **Path Finding Algorithm:** The `OptimusPath` class employs a path-finding algorithm to traverse the grid, considering priority rules and handling special symbols along the way.
- **Teleportation Support:** The class supports teleportation within the grid, enabling movement between teleportation points.
- **teleMap** is a dictionary used to store teleportation mappings within the grid. It maps the keys representing the coordinates of one teleportation point to the coordinates of another teleportation point. This dictionary enables efficient teleportation of the Optimus character from one point to another within the grid.

- **Grid Movement:** The class facilitates movement of the Optimus character within the grid.
- **Obstacle Detection:** It checks for obstacles in the grid to determine valid movement paths.
- **Path Finding Algorithm:** The `OptimusPath` class employs a path-finding algorithm to traverse the grid, considering priority rules and handling special symbols along the way.
- **Teleportation Support:** This feature supports teleportation within the grid, enabling movement between teleportation points.
- **BreakerMode Support:** This feature supports the breaker mode within the grid, enabling the Optimus to take the path having 'X' obstacles
- **InvertMode Support:** This feature supports the reversal of direction prioritization for Optimus.
- **Direction Enumeration:** The class utilizes an enum called `Direction` to represent cardinal directions: SOUTH, EAST, NORTH, and WEST.
- **Priority Enumeration:** Another enum named `Priority` defines two priority sequences for directions: SOUTHEASTNORTHWEST and WESTNORTHEASTSOUTH.
- **Special Symbols:** Special symbols such as 'I' (INVERT) and 'B' (BREAKMODE) are represented using the `SpecialSymbol` enum to indicate special functionalities.



## Variables

- **x, y:** Current position of the Optimus character within the grid.
- **direction:** Optional input representing the direction in which Optimus intends to move.
- **Bounds (H, W):** Height and width of the grid.
- **grid:** The grid environment containing obstacles and paths.
- **path:** List storing the path followed by the Optimus character.
- **curr_dirxn:** Current direction of the Optimus character.
- **breakmode:** Boolean indicating whether Optimus is in break mode.
- **invert:** Boolean indicating whether Optimus is in invert mode.
- **start, end:** Starting and ending positions of the Optimus character.
- **teleLoc:** Dictionary containing teleport locations.
- **teleMap:** Dictionary mapping teleport locations.


## `move` Function

The `move` function is responsible for moving the Optimus character within the grid. It takes the current position (`x`, `y`) and an optional direction as input. If no direction is provided, the function uses the current direction of Optimus. It then calculates the new position based on the given direction, checks if the new position is within the bounds of the grid and not obstructed by obstacles, and updates the Optimus's path accordingly. If the movement is successful, the function returns `True`; otherwise, it returns `False`.

## `findPath` Logic

The `findPath` method is responsible for finding the optimal path for the Optimus character within the grid. It utilizes the `move` function to navigate through the grid while considering obstacles and movement rules. The algorithm starts by initializing the queue with the starting position of Optimus and iterates through the positions in the queue until the destination is reached or a loop is detected. At each iteration, it examines the current position, checks for obstacles, updates the movement direction, and attempts to move Optimus in the selected direction. The algorithm terminates when the destination is reached, or if a loop is detected, in which case it marks the path as 'LOOP'. The discovered path is then printed as output.


## Usage

1. **Initialization:** Instantiate the `OptimusPath` class by providing the height (`H`), width (`W`), and grid (`grid`) of the environment.
2. **Finding Path:** Call the `findPath()` method to execute the path-finding algorithm and determine the optimal path from the start to the end point.
3. **Special Symbols Handling:** The algorithm handles special symbols 'I' and 'B' to manage invert mode and break mode, respectively.
4. **Printing Output:** The `printOutput()` method prints the final path discovered by the algorithm.

## Example

```python
# Example usage of OptimusPath class

# Define the grid and its dimensions
    H = 5
    W = 5
    grid = [
        ['#', '#', '#', '#', '#'],
        ['#', '@', ' ', ' ', '#'],
        ['#', ' ', ' ', '$', '#'],
        ['#', ' ', ' ', ' ', '#'],
        ['#', '#', '#', '#', '#']
    ]
    # Create an instance of OptimusPath
    optimus = OptimusPath(H, W, grid)

```
## Dependencies

- **collections:** This module is used for working with collections of data in Python.
- **enum:** This module provides support for enumerations in Python.

## Credits

- This project is maintained by Sumedha Khatter as a part of Tesla Coding Challenge.


