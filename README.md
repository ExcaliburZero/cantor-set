# cantor-set
A python script which uses a recursive function to visually generate a [Cantor set](https://en.wikipedia.org/wiki/Cantor_set).

![A screenshot of the generated Cantor set](screenshot.png)

## Algorithm
* Draw a line from the left point to the right point.
* Move to the next row.
* Draw a line from the left point to the point that is the left point plus one third of the difference between the right and left points.
* Recall the function with the left point being the current left point, and the right point being the current left point plus one third of the difference between the right and left points.
* Draw a line from the left point plus two thirds of the difference between the right and left points to the right point.
* Recall the function with the left point being the current left point plus two thirds of the difference between the right and left points, and the right point being the current right point.

## Pseudocode
```
Function (left_point, right_point)
	Draw a line from left_point to right_point
	Move to next row
	Set difference to the difference between right_point and left_point
	Draw a line from left point to left_point plus one third of difference
	Call Function (left_point, left_point plus one third of difference)
	Draw a line from left_point plus two thirds of difference to right_point
	Call Function (left_point plus two thirds of difference, right_point)
	
```

## License
This script is availible under [The MIT License](https://opensource.org/licenses/MIT), see the `LICENSE` file for more information.
