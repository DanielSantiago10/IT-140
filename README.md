# M.O.M Text Adventure

## Phase 1: Conceptualization and Story Telling

**The Narrative:** Definedd the hero Syrus, and the antagonist, M.O.M. (Short for Maddened Opinionated Mephistophelian)

**World Building:** Mapped out the house as a dungeon. I designed a layout where the "Porch" is the starting zone and the "Basement" is the final boss room.

**Mapping:** Created a visual flow of the house to ensure everyroom was interconnected and accessible via cardinal directions (North, South, East, West)

## Phase 2: Logic and Flow Design (Pseudocode)

**Movement Logic:** I used a flowchart to map how the program should handle user input. I decided to program must validate whether a direction is "Valid"(has a connecting room) before moving the player.

**Inventory Logic:** Designed a system to check if a room contains an item and how the player interacts with it.  Thi ensured the player couldn't reach the "Win State" without oollecting all six items first.

## Phase 3:** Technical Implementation (The Code)

**Data Structures:** I utilized Dictionaries to store the house map (rooms) and the item locations (items). This allowed for $O(1)$ lookup time when Syrus moves or searches.

**Game Loop:** Implemented a while loop to keep the game running until a "Win" or "Loss" condition is met.

**State Management:** Created a get_new_state function to handle the transition between rooms based on user input, ensuring the player’s location is updated dynamically.

**The Boss Encounter:** Coded a specific "Argueing with M.O.M." sequence in the Basement using a nested loop delay to build tension before checking the win condition (Inventory Count = 6).

## Phase 4:** IDE Refinement(The Pycharm experience)

**Error Handling:** Used PyCharm’s real-time linting (the red/yellow bulbs) to catch syntax errors and "dead code" (the dull grey highlights).

**Code Completion:** Leveraged IntelliSense to speed up the writing of repetitive structures like print statements and dictionary keys.

**Refactoring:** Used the color-coding system to visually organize the code, making it easier to distinguish between built-in functions, strings, and variables.


