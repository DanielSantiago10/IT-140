To showcase your PowerPoint presentation effectively on GitHub, you should convert the visual and logical elements into a structured **Project Documentation** file using Markdown (`.md`). This allows recruiters to see your design process, narrative skills, and logical planning without needing to download a file.

Here is a GitHub-ready format for your project, titled `DESIGN_DOCUMENTATION.md`.

---

# 🎮 M.O.M. Adventure: Game Design & Storyboard

**Project:** Text-Based RPG Logic & Narrative

**Developer:** Daniel Santiago 

**Date:** 4 April 2021 

---

## 📖 Narrative & Objective

The game follows **Syrus**, a teenager who believes he is playing video games to save the world. However, a "hideous beast" stands in his way: the **Maddened Opinionated Mephistophelian**, or **M.O.M.**.

* **The Mission:** Syrus must navigate the "underworld" (his house) to complete a set of quests known to normies as "cleaning the house".


* **The Goal:** Collect all belongings and present them to M.O.M. in the basement to win her approval.


* **The Stakes:** Failure results in being "grounded," which in Syrus's mind, means the world ends.



---

## 🗺️ World Map & Item Locations

The "Dungeon" layout is mapped across eight distinct zones, each containing a specific item required for the final encounter.

| Room | Item to Collect |
| --- | --- |
| **Porch** | Starting Zone |
| **Mud Room** | Underwear  |
| **Dining Room** | Right Sock |
| **Kitchen** | Sweater |
| **Living Room** | Under Shirt |
| **Bathroom** | Left Sock |
| **Brother's Room** | Shirt |
| **Basement** | **Final Boss: M.O.M.**|

---

## 🛠️ Logical Framework

The game's mechanics are driven by two primary flowcharts that handle movement and inventory management.

### 1. Movement Logic

The program facilitates movement by requesting cardinal directions (coordinates) and validating them against the map boundaries.

* **Start:** Request input from the player.


* **Validation:** Check if the direction is valid for the current room.


* **Execution:** If valid, move Syrus to the "Next Room" and ask for the next action.



### 2. Inventory Management

This logic ensures Syrus can interact with items found in each room and correctly update his status.

* **Interaction:** Upon entering a room, the game displays available items and asks the player if they wish to pick them up (Y/N).


* **Validation:** The system validates the input and item availability.


* **Update:** If successful, the action is performed, the item is added to "Save Inventory," and the current status is displayed.



---

## 🏁 Win/Loss Conditions

* **Victory:** Collect all 6 items and reach the Basement to gain M.O.M.'s approval.


* **Defeat:** Facing M.O.M. without the required items or making incorrect choices results in the "Grounded" state.



---

### 🚀 How to use this on GitHub:

1. **Create a folder** in your repo called `/docs`.
2. **Upload your actual `.pptx` file** there (so people can still download the original).
3. **Create the `DESIGN_DOCUMENTATION.md` file** using the text above.
4. **Link it in your README:** > 🎨 **Design & Storyboarding:** Check out the [Original Game Presentation](https://www.google.com/search?q=./docs/DESIGN_DOCUMENTATION.md) to see the narrative and logical flowcharts.

**Would you like me to help you draft a "Project Gallery" section for your Wix portfolio using these same details?**
