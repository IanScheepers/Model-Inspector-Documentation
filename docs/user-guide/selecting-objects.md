# Selecting Objects

Model Inspector only inspects objects you've explicitly added to its **Objects to Inspect** list. It will automatically try to scan your whole scene. 

## Adding objects

![The Model Inspector panel with the Add Object button highlighted](../assets/images/getting-started-add-objects-to-inspect.png){ style="display: block; margin: 0 auto;" }

1. Select one or more objects in the viewport or the Outliner.
2. In the *Objects to Inspect* box, click the ➕ button.

Every currently-selected object is added. If you attempt to add objects already in the list, they will be ignored, so it's safe to select overlapping groups and add repeatedly if you wish, as you won't get duplicate entries.

!!! tip
    You can build the list incrementally: select a few objects and add them, then select more and add again. The list keeps growing until you clear it.

## Removing objects


![The Model Inspector panel with the Add Object button highlighted](../assets/images/user-interface-selecting-objects.png){ style="display: block; margin: 0 auto;" }

- Click a row to make it the active entry, then click ➖ to remove just that object.
- Click 🗑 **Clear List** to remove every object at once. This also clears all stored results and turns off any active viewport overlays.

## Objects that no longer exist

If an object referenced in the list is deleted from the scene, its row shows **`<missing object>`**. Remove it with ➖ or clear the whole list.

Next: [Running an Inspection](running-inspections.md).
