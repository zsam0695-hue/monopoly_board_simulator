# CS210 Programming Assignment
## Monopoly Board Simulator (Spring 2026)
## Overview
This program simulates a simplified Monopoly game board using a **circular linked list**. The board is made up of spaces that loop endlessly, allowing a player to move around the board by rolling dice. Each space has information like the property name, color, value, and rent.
The main goal of this project is to demonstrate pointer-based traversal, circular list structure, and the games movement logic without using array indexing.
---
## Features
- Implements a **circular linked list** to represent the Monopoly board.
- Supports adding single or multiple spaces.
- Enforces a **max of 40 spaces**.
- Allows player movement around the board.
- Tracks how many times the player passes GO.
- Prints some or all of the board.
- Has an advanced feature that **mirrors** the board.
- **Safely** empties the board when program is done.
---
## Data Structures Used
### MonopolySpace - A class that represents each space on the board.
**Attributes:**
- propertyName: name of the space
- propertyColor: color group
- value: buying value of the property
- rent: cost of rent
**Methods:**
- isEqual(): compares two spaces by name
- print(): prints the space's details
### Node<T> - A template class representing a node in the linked list.
**Attributes:**
- data: stores a MonopolySpace object
- nextNode: pointer to the next node
### CircularLinkedList<T> - A template class that manages the board.
**Key Attributes:**
- headNode: first node in the list
- tailNode: last node in the list, and points back to head
- playerNode: pointer representing the player's current position
- nodeCount: number of spaces on the board
- passGoCount: number of times the player passes GO


### README
Your `README.md` must include:
- Build and run instructions.
- Description of data structures used.
- A complete list of functions with short explanations.
- Explanation of traversal and movement logic.
- Explicit mention of the **40-space board limit**.
---
## Submission
- Submit the GitHub repository link on Canvas.
- No zip files.
- Late submissions follow standard course policy.
