# Running an Inspection

Once you have [objects added](selecting-objects.md) and the checks you want [enabled](interface-overview.md#inspections), click **Run Inspection**.

(**TO DO ADD IMAGE**)

## What happens when you run it

1. Any results and overlays from a previous run are cleared.
2. Model Inspector builds the list of checks to run: a check only runs if **both** its category and the check itself are enabled.
3. For every object in the inspection list, every enabled check runs against that object, using Blender's evaluated dependency graph — so modifiers are taken into account.
4. Each object's results are stored and shown when you select it in the list.

## Before you run

Model Inspector will refuse to run, and report why, if:

- **You're not in Object Mode.** Switch out of Edit Mode / Sculpt Mode / etc. first.
- **The inspection list is empty.** Add at least one object.
- **No checks are enabled.** Enable at least one category and at least one check within it.

## Re-running

Running the inspection again always starts clean — it clears prior results and overlays before re-checking, so results never go stale or mix between runs. This also means overlays you had toggled on will turn off; re-enable them from the fresh results if needed.

Next: [Reading Results & Overlays](results-and-overlays.md).
