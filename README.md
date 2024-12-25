# Kotlin Collection Modification: Unexpected Behavior with removeIf

This example demonstrates a potential issue when using the `removeIf` function on Kotlin collections.  The `removeIf` function modifies the collection in-place.  Iterating and modifying a collection simultaneously can lead to unexpected results if not handled carefully.

The provided code snippets show the correct usage of `removeIf` with `MutableList`, `MutableSet`, and `MutableMap`. It is important to note that you should *not* modify the collection while iterating over it unless you use methods like `removeIf` that handle concurrent modification properly.  Attempting to modify a collection directly during iteration using a standard loop can cause exceptions.

## How to Use

1.  Save the code in `bug.kt`.
2.  Run the code using a Kotlin compiler (e.g. `kotlinc bug.kt -include-runtime -d bug.jar` and `java -jar bug.jar`).
3.  Observe the output and note that the `removeIf` function correctly removes the elements satisfying the predicate.

The `bugSolution.kt` file contains the same content, serving as a solution to the problem described.