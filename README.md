# License Plate Detection

This is an exploratory project to evaluate how we can use Meta's Segment Everything Model (SAM) to create masks for known license plates in images. 

## Custom Functions

### `show_mask`

This function takes in the following parameters :
- `mask` : a Numpy array representing the mask
- `ax` : the function that gets the current axes so that we can draw on directly
- `random_color` : a boolean that determines whether or not we use a random color to represent the mask

Purpose: The purpose of this function is to display the object's mask so that the user can see it.

### `show_box`

This function takes in the following parameters :
- `box` : These are the YOLO coordinates of the bounding box for the mask. It is a **list** that contains `[x_center, y_center, width, height]`.
- `ax` : the function that gets the current axes so that we can draw on directly.

Purpose: The purpose of this function is to display the object's bounding box in which we get from YOLO annotation file. 


### `get_coord`

This function takes in the following parameters: 
- `img` : This is the image that will be masked.
- `ann_name` : This is the file name in which the YOLO annotations are stored.

**Returns:** This returns a tuple where the first element is the label and the second is a numpy array that contains the coordinates of the top left corner and the bottom right corner in the form, `[x1, y1, x2, y2]`


### `get_txt`

This function takes in the following parameters: 
- `img_name`: path of the image

**Return:** returns the path of the annotation

