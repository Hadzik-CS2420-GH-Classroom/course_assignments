# Module 2 Assignment: GameCharacter

## Overview

In this assignment you will implement the `GameCharacter` class, a role-playing game character that practices the core C++ concepts from Module 2:

- **Constructor overloading** — writing multiple constructors with different parameter lists
- **Member initializer lists** — the preferred way to initialize members in constructors
- **Stack vs heap allocation** — understanding automatic vs manual memory management
- **`const` correctness** — marking methods that do not modify the object
- **Encapsulation** — private data members with public getter methods
- **Destructors** — observing when and how objects are destroyed

## What You Need To Do

All of your work goes in **`src/GameCharacter.cpp`**. The header (`include/GameCharacter.h`) and tests (`tests/game_character_test.cpp`) are provided for you — **do not modify them**.

Open `src/GameCharacter.cpp` and follow every `TODO` comment. Each section tells you exactly what to implement and includes hints referencing patterns from the Code-Together activities.

### Checklist

1. **Default constructor** — no arguments, uses member initializer list
2. **Single-argument constructor** — takes a name
3. **Two-argument constructor** — takes name and character class
4. **Four-argument constructor** — takes name, class, level, and hit points
5. **Destructor** — prints a message when the object is destroyed
6. **Four getter methods** — `getName()`, `getCharacterClass()`, `getLevel()`, `getHitPoints()`
7. **`isAlive()`** — returns whether hit points are above zero
8. **`getSummary()`** — returns a formatted string of the character's info
9. **`print()`** — prints the summary to the console


## Expected Output (when all TODOs are complete)

When you run the program, you should see output similar to:

```
=== GameCharacter: Constructor Overloading & Memory Demo ===

1) Default constructor:
   [Unknown] Class: Warrior, Level: 1, HP: 100

2) Single-argument constructor (name only):
   [Aragorn] Class: Warrior, Level: 1, HP: 100

3) Two-argument constructor (name and class):
   [Gandalf] Class: Mage, Level: 1, HP: 100

4) Four-argument constructor (fully specified):
   [Legolas] Class: Ranger, Level: 15, HP: 130

--- Utility Methods ---
5) Is Legolas alive? Yes
6) Is Boromir alive? No

--- Stack vs Heap Allocation ---
7) Heap-allocated (new/delete):
   [Gimli] Class: Warrior, Level: 12, HP: 180
GameCharacter destroyed: Gimli

--- Heap Array ---
8) Enter party size: 3
   Heap array of 3 default characters:
   [0] [Unknown] Class: Warrior, Level: 1, HP: 100
   [1] [Unknown] Class: Warrior, Level: 1, HP: 100
   [2] [Unknown] Class: Warrior, Level: 1, HP: 100
GameCharacter destroyed: Unknown
GameCharacter destroyed: Unknown
GameCharacter destroyed: Unknown

--- Observe Destructor Messages ---
Watch the destructor messages below as main() returns.
Stack objects (c1-c4, fallen) will be destroyed automatically.

GameCharacter destroyed: Boromir
GameCharacter destroyed: Legolas
GameCharacter destroyed: Gandalf
GameCharacter destroyed: Aragorn
GameCharacter destroyed: Unknown
```

## Grading (60 points)

| Category | Points | What is tested |
|---|---|---|
| Build | 4 | Project compiles without errors |
| Default constructor | 8 | Sets name, class, level, HP to defaults |
| Single-arg constructor | 8 | Sets name, defaults for class/level/HP |
| Two-arg constructor | 8 | Sets name and class, defaults for level/HP |
| Four-arg constructor | 8 | Sets all four members |
| isAlive() | 4 | Returns true/false based on HP |
| getSummary() | 8 | Returns correctly formatted string |
| print() | 4 | Outputs character info to console |
| Heap allocation | 4 | Single heap object works with new/delete |
| Heap array | 4 | Array of objects works with new[]/delete[] |
| **Total** | **60** | |
