# Banalization
Remove the demarcation from a gray scale document image (written in Hebrew).

##How to Run:
When you run the program it activates a for loop which calls a function for demarcation removal on (Example1-Example4.png).
This triggers a mask to the original photos' demarcations and the result are new images (result1-result4.png) that are saved in the current directory.

##How it Works:
We first change the original photo into binary photo of black/white using threshold of 150. Then we loop on all the contours in the photo and find their sizes.
We then find the maximal size and determine the contours' threshold to be applied on the photo in order to delete the demarcations (which will be smaller in size).
####fun changeDemColor:
Determines the threshold and deletes the demacrations accordingly.
####fun getMaxVal:
Traverses the contours and finds the maximal size contour.
fun demarcation_removal:
Wraps the whole program and triggers the above functions and then calls imwrite to save the results.


