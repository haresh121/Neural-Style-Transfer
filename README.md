# Style Transfer

Style Transfer is a process in which we strive to modify the style of an image while preserving its content. Given an input image and a style image, we can compute an output image with the original content but a new style.


Check out the Medium article on this:

[Neural Style Transfer - Style Transfer by CNN](https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-neural-style-transfer-ef88e46697ee)

<h3 align="center">
  <img src="assets/combined.png">
</h3>

# How does it work?
1. We take input image and style images and resize them to equal shapes.
2. We load a pre-trained CNN (VGG16).
3. Knowing that we can distinguish layers that are responsible for the style (basic shapes, colors etc.) and the ones responsible for the content (image-specific features), we can separate the layers to independently work on the content and style.
4. Then we set our task as an optimization problem where we are going to minimize:
	* **content loss** (distance between the input and output images - we strive to preserve the content)
	* **style loss** (distance between the style and output images - we strive to apply a new style)
	* **total variation loss** (regularization - spatial smoothness to denoise the output image)

# Results

## Input

<h3>
  <img src="assets/input.png" width="500">
</h3>


## Style
 
<h3>
  <img src="assets/style.png" width="500">
</h3>


## Output

### 1 iteration
<h3>
  <img src="assets/1.png" width="500">
</h3>

### 5 iterations
<h3>
  <img src="assets/5.png" width="500">
</h3>

### 10 iterations
 
<h3>
  <img src="assets/10.png" width="500">
</h3>

### 15 iterations
 
<h3>
  <img src="assets/15.png" width="500">
</h3>
[**GITHUB**](https://github.com/haresh121)

