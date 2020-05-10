## Fisheye-Dewarping

### Background
There is an object in Lexivalley Inc. which offers real-time alerts to nearby drivers 
when there is an accident or impaired driving event happening around the area. 
The project belongs to the categories of computer vision and vehicle-to-everything (V2X).

Demanded by this project, the circular fisheye camera image should be warped into a flat image.
The input is a video from fisheye camera. The output should be a dewarped video.

### Useful resourses
1. py-fisheye-dewarp:

   https://github.com/BlueHorn07/py-fisheye-dewarp

   https://github.com/BlueHorn07/py-fisheye-dewarp/wiki/(ENG)-Fisheye-Dewarp
   
The main idea is that fisheye image can be treated as a kind of sphere's projection image. 
Therefore we can imagine the fisheye image as surface of a sphere.
Next, the pixel in the spehre surface can be transfered to longitude / latitude coordinate, 
like world map.
In brief, the procedure can be illustrated as below:
fisheye → spherical → longitude/latitude.

### Progress:
1. First, we check if the candidate code is workable.
   We use PyCharm to create an object and run the code, and it works.
2. Study the paper "A practical distortion correcting method from fisheye image to perspective projection image" to understand the mechanism of the code, which is essential to modify the code as we want.
3. Study "opencv" which is the tool for converting between vedio and image.
