# CS210 Programming Assignment
## Monopoly Board Simulator (Spring 2026)
## Overview
This program simulates a simplified Monopoly game board using a **circular linked list**. The board is made up of spaces that loop endlessly, allowing a player to move around the board by rolling dice. Each space has information like the property name, color, value, and rent.
The main goal of this project is to demonstrate pointer-based traversal, circular list structure, and the games movement logic without using array indexing.

### Board Construction
The board is built in the `main()` function **before** the game starts. Spaces are hardcoded using a `vector<MonopolySpace>` and then added to the list with `addMany()`.

**Note:** 
There is a 40 space board limit which cannot be exceeded!
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
## Build and Run Instructions
### Build
`g++ -std=c++17 main.cpp -o monopoly_board`
### Run
`./monopoly_board`

---
## Data Structures Used
### *MonopolySpace* : A class that represents each space on the board.
**Attributes:**
- `propertyName`: name of the space
- `propertyColor`: color group
- `value`: buying value of the property
- `rent`: cost of rent

**Methods:**
- `isEqual()`: compares two spaces by name
- `print()`: prints the space's details


### *Node<T>* : A template class representing a node in the linked list.
**Attributes:**
- `data`: stores a `MonopolySpace` object
- `nextNode`: pointer to the next node


### *CircularLinkedList<T>* : A template class that manages the board.
**Key Attributes:**
- `headNode`: first node in the list
- `tailNode`: last node in the list, and points back to head
- `playerNode`: pointer representing the player's current position
- `nodeCount`: number of spaces on the board
- `passGoCount`: number of times the player passes GO


**Core Functions:**

Core A
- `addSpace(...)`: Adds a new node to the tail, maintains circular structure, enforces max size 40, returns success/failure beyond capacity.

Core B
- `addMany(...)`: Adds spaces sequentially, stops exactly at capacity, returns how many were added, and does not corrupt pointers.

Core C
- `movePlayer(int n)`: Moves a player cursor forward by `n` steps node-by-node, wraps around, and tracks how many times the player passes GO.
- `getPassGoCount()`: Returns how many times the player has passed GO.

Core D
- `printFromPlayer(int count)`: Prints a fixed number of spaces starting from the player, with a safe stop condition (no infinite loops).
- `printBoardOnce()`: Prints the whole board once.


**Other Functions:**

Advanced Option B
- `mirrorBoard()`: Reverses the traversal direction of the circular linked list.

Edge-Case Helper
- `countSpaces()`: Counts the number of spaces.

Cleanup
- `clear()`: Deletes all the nodes and empties the board, resetting all the attributes.
---
## Traversal and Movement Logic
The player starts at the head of the list, which is the GO space. Each turn, the player rolls two dice and moves forward from 2-12 spaces using the `nextNode` pointers. If the player passes the tail node, then `passGoCount` increases by one, simulating passing GO.
