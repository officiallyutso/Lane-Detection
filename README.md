# Advanced Lane Detection with Computer Vision

## Project Overview

This project implements a sophisticated lane detection system using advanced computer vision techniques in Python. The application can detect lane lines in both images and video streams, demonstrating robust lane line identification across various driving conditions.

## Features

- Detect white and yellow lane lines in different color spaces
- Process images and video streams in real-time
- Apply multiple image processing techniques:
  - Color selection
  - Grayscale conversion
  - Gaussian smoothing
  - Canny edge detection
  - Region of interest selection
  - Hough line transformation
- Adaptive lane line drawing with slope and length weighting

## Prerequisites

- Python 3.7+
- Libraries:
  - OpenCV (`cv2`)
  - NumPy
  - Matplotlib
  - MoviePy
  
## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/lane-detection.git
   cd lane-detection
   ```

2. Install required dependencies:
   ```bash
   pip install opencv-python numpy matplotlib moviepy
   ```

## Detailed Processing Pipeline

The lane detection pipeline consists of several key stages:

1. **Color Space Conversion**
   - Convert images to different color spaces (RGB, HSV, HSL)
   - Isolate lane line colors (white and yellow)

2. **Image Preprocessing**
   - Convert to grayscale
   - Apply Gaussian blur to reduce noise
   - Detect edges using Canny edge detection

3. **Region of Interest Selection**
   - Mask out irrelevant parts of the image
   - Focus on the road ahead

4. **Line Detection**
   - Use Hough Transform to identify line segments
   - Compute line slopes and intercepts
   - Distinguish between left and right lane lines

5. **Lane Line Rendering**
   - Draw smooth, continuous lane lines
   - Overlay detected lines on original image/video

## Example Usage

### Image Lane Detection
```python
# Process a single image
result = frame_processor(input_image)
plt.imshow(result)
plt.show()
```

### Video Lane Detection
```python
# Process a video file
process_video('input_video.mp4', 'output_video.mp4')
```

## Detailed Functions

### Key Functions
- `HSL_color_selection()`: Color-based lane line isolation
- `canny_detector()`: Edge detection
- `region_selection()`: Focus area determination
- `hough_transform()`: Line segment identification
- `lane_lines()`: Compute full lane line coordinates
- `draw_lane_lines()`: Render lane lines on image

## Limitations and Potential Improvements

- Performance may vary in challenging lighting conditions
- Sensitive to camera positioning and road surface
- Does not handle curved lanes optimally

# Output Images

https://github.com/user-attachments/assets/89383980-80be-4d20-9aad-b0cc0b04ddab

Example image:

https://github.com/user-attachments/assets/8cc39266-5565-4d77-9d5f-28aab7ae776d


## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a pull request

## License

This project is open-source, licensed under the MIT License.

## Acknowledgments

- OpenCV Community
- Computer Vision research resources

## References

- Udacity Self-Driving Car Nanodegree Program
- OpenCV Documentation
- Advanced Lane Detection Techniques in Computer Vision

## Contact

For questions or collaboration, please open an issue or contact Utso Sarkar.
