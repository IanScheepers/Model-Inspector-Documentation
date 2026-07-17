# Running an Inspection

Once you have [objects added](selecting-objects.md) and the checks you want [enabled](interface-overview.md#inspections), click **Run Inspection**.

(**TO DO ADD IMAGE**)

## What happens when you run it

1. Any results and overlays from a previous run are cleared.
2. Model Inspector builds the list of checks to run: a check only runs if **both** its category and the check itself are enabled.
3. For every object in the inspection list, every enabled check runs against that object, using Blender's evaluated dependency graph — so modifiers are taken into account.
4. Each object's results are stored and shown when you select it in the list.
5. Once every object has been checked, Blender's status bar reports how many objects were inspected and how long it took, e.g. `Ran tests on 3 object(s) in 0.42s`. Use it to gauge how much a run costs before scaling up to a bigger batch of objects.

## Before you run

Model Inspector will refuse to run, and report why, if:

- **You're not in Object Mode.** Switch out of Edit Mode / Sculpt Mode / etc. first.
- **The inspection list is empty.** Add at least one object.
- **No checks are enabled.** Enable at least one category and at least one check within it.

## Large meshes

Before running, Model Inspector totals the **evaluated** vertex count (post-modifier) across every object in the inspection list. If that total is above 100,000 vertices, clicking **Run Inspection** first shows a confirmation dialog warning that the inspection may take a while and suggesting you save your file first:

> Inspecting *N* vertices. This may take some time to complete. Consider saving before running this operation.

Confirm to run the inspection anyway, or cancel to trim your object list first. Once this threshold is crossed, the panel also keeps a **High vertex count** warning visible below the Run Inspection button as a standing reminder.

## Re-running

Running the inspection again always starts clean — it clears prior results and overlays before re-checking, so results never go stale or mix between runs. This also means overlays you had toggled on will turn off; re-enable them from the fresh results if needed.

Next: [Reading Results & Overlays](results-and-overlays.md).
