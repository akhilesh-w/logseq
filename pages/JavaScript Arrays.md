- Technically a type of [object]([[JavaScript Objects]])
  id:: 64777862-c7c8-47db-b7b6-6222360d6836
-
- ### Arrays
	- Bracket notation: `[0]`
	- *Zero based indexing*: The first character is `0`, not `1`
	- You can get arrays within arrays like so: `myArray = [[1,2,3],["A", "B", "C"][4,5,6]]`
	- And access `5` like so: `myArray[2,1]`
	- `.push` appends to array
	- `.pop` removes and returns the last element
	- `.shift` removes and retuns the first element
	- `.unshift` adds elements to the beginning
-
- ### Methods
	- push adds to end, pop removes at end
	- unshift adds to end, shift removes at end
	- splice(2,2) removes at index two a number of two elements
		- the third parameter of splice adds elements
	- slice(1,3) only copies over without deleting - from index 1 to index 3
-
- ### Filter
	- ```JavaScript
	  const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
	  
	  const result = words.filter(word => word.length > 6);
	  
	  console.log(result);
	  // expected output: Array ["exuberant", "destruction", "present"
	  ```
-
-