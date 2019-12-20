# Coin-Detector
First detected the coins then drew vertical lines for the coins that fall under the same straight line using OpenCV. 

*Function used*
In order to detect circles in images, we’ll need to make use of the *cv2.HoughCircles* function. It’s definitely not the easiest function to use, but with a little explanation, I think we’ll get it.

> cv2.HoughCircles(image, method, dp, minDist)

- image: 8-bit, single channel image. If working with a color image, convert to grayscale first.
method: Defines the method to detect circles in images. Currently, the only implemented method is cv2.HOUGH_GRADIENT, which corresponds to the Yuen et al. paper.
- dp: This parameter is the inverse ratio of the accumulator resolution to the image resolution (see Yuen et al. for more details). Essentially, the larger the dp gets, the smaller the accumulator array gets.
- minDist: Minimum distance between the center (x, y) coordinates of detected circles. If the minDist is too small, multiple circles in the same neighborhood as the original may be (falsely) detected. If the minDist is too large, then some circles may not be detected at all.
- param1: Gradient value used to handle edge detection in the Yuen et al. method.
- param2: Accumulator threshold value for the cv2.HOUGH_GRADIENT method. The smaller the threshold is, the more circles will be detected (including false circles). The larger the threshold is, the more circles will potentially be returned.
- minRadius: Minimum size of the radius (in pixels).
- maxRadius: Maximum size of the radius (in pixels).
