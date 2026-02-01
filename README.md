# M.O.M Text Adventure

## Phase 1: Conceptualization and Story Telling

**The Narrative:** Definedd the hero Syrus, and the antagonist, M.O.M. (Short for Maddened Opinionated Mephistophelian)

![Desc](https://github.com/DanielSantiago10/M.O.M.-Text-Adventure-RPG/blob/main/Images/Story%20Board%20Desc.png)

**World Building:** Mapped out the house as a dungeon. I designed a layout where the "Porch" is the starting zone and the "Basement" is the final boss room.
```
rooms = {
    'Porch': {'East': 'Mud Room'},
    'Mud Room': {'North': 'Bathroom', 'West': 'Porch', 'South': 'Dining Room', 'East': 'Living Room', },
    'Dining Room': {'North': 'Mud Room', 'East': 'Kitchen', },
    'Kitchen': {'West': 'Dining Room', 'Item': 'sweater'},
    'Bathroom': {'South': 'Mud Room', 'East': 'Brothers Room', },
    'Brothers Room': {'West': 'Bathroom', 'Item': 'shirt'},
    'Living Room': {'North': 'Basement', 'West': 'Mud Room', },
    'Basement': {'South': 'Living Room', 'Item': 'M.O.M.'},
}

items = {
    'Mud Room': 'underwear',
    'Dining Room': 'right sock',
    'Kitchen': 'sweater',
    'Bathroom': 'left sock',
    'Brothers Room': 'shirt',
    'Living Room': 'under shirt',
    'Basement': 'M.O.M.',
}
```

**Mapping:** Created a visual flow of the house to ensure everyroom was interconnected and accessible via cardinal directions (North, South, East, West) 

![Mapping](https://github.com/DanielSantiago10/M.O.M.-Text-Adventure-RPG/blob/main/Images/Storyboard%20Map.png)

## Phase 2: Logic and Flow Design (Pseudocode)

**Movement Logic:** I used a flowchart to map how the program should handle user input. I decided to program must validate whether a direction is "Valid"(has a connecting room) before moving the player. 
```
def get_new_state(state, directions):  # start with what state you are in
    new_state = state  # everytime the state of the char updates
    for i in rooms:
        if i == state:
            if directions in rooms[i]:
                new_state = rooms[i][directions]

    return new_state  # return
```

![Room Logic](https://github.com/DanielSantiago10/M.O.M.-Text-Adventure-RPG/blob/main/Images/Room%20Logic.png)

**Inventory Logic:** Designed a system to check if a room contains an item and how the player interacts with it.  Thi ensured the player couldn't reach the "Win State" without oollecting all six items first.

![Inventory Logic](https://github.com/DanielSantiago10/M.O.M.-Text-Adventure-RPG/blob/main/Images/Inventory%20Logic.png)

## Phase 3:** Technical Implementation (The Code)

**Data Structures:** I utilized Dictionaries to store the house map (rooms) and the item locations (items). This allowed for $O(1)$ lookup time when Syrus moves or searches.

**Game Loop:** Implemented a while loop to keep the game running until a "Win" or "Loss" condition is met.
```while 1:
    print('You are in ', state)  # lets the char know what state they are in
    if state == 'Basement':
        print('Argueing with M.O.M.', end='')
        for i in range(50):
            for j in range(1000000):
                pass
            print(".", end='', flush=True)
        print()
        if len(inventory) == 6:
            print('You won M.O.M over!! now Syrus can save the World!!')
        else:
            print('Sorry, you lost - You are grounded')
        break
```

**State Management:** Created a get_new_state function to handle the transition between rooms based on user input, ensuring the player’s location is updated dynamically.

```
print('Available to you in this room is', items[state])
    print('You currently have', inventory)
    direction = input('Enter Which direction you want to go East, West, North, South or enter exit: ')
    if items[state] in inventory:
        pass
    else:
        inventory.append(items[state])
        continue
    direction = direction.capitalize()  # gives the char direction on how to play
    if direction == 'Exit':
        print('Thank you for playing!')
        exit(0)
    if direction == 'East' or direction == 'West' or direction == 'North' or direction == 'South':
        new_state = get_new_state(state, direction)
        if new_state == state:  # if
            print('The room has wall in that direction pick another direction')
        else:
            state = new_state
    else:
        print('Invalid command!')
```

**The Boss Encounter:** Coded a specific "Argueing with M.O.M." sequence in the Basement using a nested loop delay to build tension before checking the win condition (Inventory Count = 6).



## Phase 4:** IDE Refinement(The Pycharm experience)

**Error Handling:** Used PyCharm’s real-time linting (the red/yellow bulbs) to catch syntax errors and "dead code" (the dull grey highlights).

**Code Completion:** Leveraged IntelliSense to speed up the writing of repetitive structures like print statements and dictionary keys.
```
if state == 'Basement':
        print('Argueing with M.O.M.', end='')
        for i in range(50):
            for j in range(1000000):
                pass
            print(".", end='', flush=True)
        print()
        if len(inventory) == 6:
            print('You won M.O.M over!! now Syrus can save the World!!')
        else:
            print('Sorry, you lost - You are grounded')
```
**Refactoring:** Used the color-coding system to visually organize the code, making it easier to distinguish between built-in functions, strings, and variables.


