## Fisheye-Dewarping

### Background
There is an object in `Lexivalley Inc`. which offers real-time alerts to nearby drivers 
when there is an accident or impaired driving event happening around the area. 
The project belongs to the categories of `Computer Vision` and `Vehicle-to-Everything` (V2X).

<img src="https://github.com/yuhang2685/Fisheye-Dewarping/blob/master/frame269.jpg" width="60%">

Demanded by this project, the circular `fisheye` camera image should be warped into a flat image.
The input is a video from fisheye camera. The output should be a dewarped video.

### Useful reference
1. [py-fisheye-dewarp](https://github.com/BlueHorn07/py-fisheye-dewarp/wiki/(ENG)-Fisheye-Dewarp)
   
The main idea is that fisheye image can be treated as a kind of sphere's projection image. 
Therefore we can imagine the fisheye image as surface of a sphere.
Next, the pixel in the spehre surface can be transfered to longitude / latitude coordinate, 
like world map.
In brief, the procedure can be illustrated as below:
fisheye → spherical → longitude/latitude.

It seems like the code is unfinished. The based on paper has no public codes.

2. [Calibrate fisheye lens using OpenCV](https://medium.com/@kennethjiang/calibrate-fisheye-lens-using-opencv-333b05afa0b0)

### Progress:
1. First, we check if the code of reference-1 "py-fisheye-dewarp" is workable.
   We use PyCharm to create an object and run the code, and it works.
2. Study the paper "A practical distortion correcting method from fisheye image to perspective projection image" (which is reference-1 based on) to understand the mechanism of the code, which is essential to modify the code as what we want.
3. Study `OpenCV` which is the tool for converting between vedio and image.
4. Conduct experiments on codes from reference-2.
5. Modify the parameters intrinsic to the camera lens to undistort the captured video image.

![screenshot](https://github.com/yuhang2685/Fisheye-Dewarping/blob/master/frame269.jpg)
![screenshot](https://github.com/yuhang2685/Fisheye-Dewarping/blob/master/frame269_undistorted.jpg)

