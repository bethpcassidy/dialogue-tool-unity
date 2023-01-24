# Dialogue Tool

This is a prebuilt simple dialogue tool made in Unity that allows for easily triggered dialogue.

This is the file that contains all of the scripts for the character objects and view objects.

## Breakdown

# Character.cs

- Controls Movement

- Creates static public bool canMove

- On start the character can move and grabs controller with a get component

- Update takes inputs for character movement and then sets up a conditional to make a character move

# ShowTextTrigger.cs

- A simple trigger that starts ShowText.cs based upon set paramaters, in this case it is when the player object enters an empy mesh.

# ShowText.cs

- On start, object is inactive

- If the attached object is triggered then dialogue box is set active, the attached object is set to active, and the line index is set to 0. Additionally, canMove is set to false, stopping character movement during dialogue.

- On exit the object is set to inactive and the lineIndex is also set to 0 to also allow for additional looping.

# Dialogue.cs

- Handles dialogue after it is triggered, and processes script data from .txt files to be outputted line by line and 1 character at a time.

- Is dropped onto the a TMPro object, that is meant to contain dialogue within a Canvas hiearchy.
