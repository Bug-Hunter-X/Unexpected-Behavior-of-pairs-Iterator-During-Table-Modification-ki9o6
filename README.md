# Lua pairs Iterator Unexpected Behavior

This repository demonstrates an uncommon Lua code error related to the `pairs` iterator's behavior when tables are modified during iteration, especially within nested structures.

## The Bug

The `bug.lua` file contains a function `foo` that recursively traverses a nested table using `pairs`.  Modifying the table while iterating with `pairs` can lead to unpredictable results. Although the current example does not crash, the behavior is not deterministic and changes depending on the table and the modification.

## The Solution

The `bugSolution.lua` file offers a solution to handle this problem by using a copy of the table for iteration, thereby avoiding modification during iteration, ensuring predictable and consistent results. This method is more robust than iterating the table directly, improving the code's reliability and preventing unexpected behavior.