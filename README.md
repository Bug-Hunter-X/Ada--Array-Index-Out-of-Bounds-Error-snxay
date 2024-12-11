# Ada Array Index Out of Bounds Bug

This repository demonstrates a common error in Ada programming: accessing an array element outside its defined bounds. The `bug.ada` file contains code that attempts to iterate through an array using an incorrect index range, resulting in a runtime error.  The `bugSolution.ada` file provides the corrected version.

**Error:** The original code uses `My_Arr'Range` which is the range of the type, not the actual indices of the array.  This is incorrect and causes a runtime error when the loop index exceeds the actual upper bound of the array.

**Solution:** The solution replaces `My_Arr'Range` with `My_Arr'First..My_Arr'Last`, which correctly iterates through the valid indices of the array.