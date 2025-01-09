# **Automania 2.0**

Welcome to **Automania 2.0**, the ultimate vision-based robotics challenge! 🚗💨  

In this hackathon, you will develop a complete vision system for a **TurtleBot3** to autonomously navigate an environment. You’ll work with cameras, detect lanes and objects, measure distances, and train a neural network for object detection. The grand goal is to combine all these elements into a fully functional, real-time autonomous system.  

---

## **Getting Started**

### Prerequisites  
Before you begin, make sure you have:  
- A **TurtleBot3** simulation .  
- A computer with Linux installed. (Bonus points if you can implement in any other platform)  
- Python or C++ environment set up with OpenCV, PyTorch, TensorRT, and other dependencies.  

---

## **Challenge Overview**

### 1. **Accessing the Camera**
- Connect the camera in simulation with turtlebot.  
- Use Python or C++ to capture images.  
- Save this part of your work as **`camera.py`** or **`camera.cpp`**.  

---

### 2. **Camera Calibration & Distance Measurement**
- **Calibrate the Camera:** Use checkerboard images to calculate the camera's intrinsic parameters.  
- **Measure Distances:** Develop a function to calculate distances to objects on the ground using pixel locations.  
- Use the provided `cone_x40cm.png` image to determine the camera’s mounting height.  
- Test your distance calculation with `cone_unknown.png`.  
- Save this part of your work as **`distance.py`** or **`distance.cpp`**.  

---

### 3. **Lane Detection**
- Process the provided image to detect yellow lane markers.  
- Use the **HSV color space** and other tools like contour detection to highlight lanes.  
- Overlay green edges or masks on detected lanes.  
- Save this part of your work as **`lane.py`** or **`lane.cpp`**.  

---

### 4. **Object Detection Neural Network**
#### Train a Neural Network:  
- Use the labeled dataset and training notebook provided.  
- Adjust parameters like **batch size**, **learning rate**, and **channels** to optimize training.  
- Train a model to detect objects and achieve reasonable accuracy.

#### Deploy with TensorRT:  
- Convert the trained model to **TensorRT** using the ONNX format.  
- Write a function to process images, run inference, and handle results efficiently.  
- Experiment with FP32 and FP16 models to compare performance.  
- Save this part of your work as **`convert_trt.py`**, **`convert_trt.cpp`**, **`detection.py`**, or **`detection.cpp`**.  

---

### 5. **Integration**
- Combine all components into a single package that:  
  1. Captures images from the TurtleBot3 camera.  
  2. Detects lanes and objects.  
  3. Calculates distances to detected objects using the bounding box.  

- Save this final system as **`integrated.py`** or **`integrated.cpp`**.  

---

## **Grading Criteria**
| **Task**                  | **Points** |
|---------------------------|------------|
| Accessing the Camera       | 10         |
| Distance Measurement       | 15         |
| Lane Detection             | 20         |
| Network Training           | 15         |
| TensorRT Deployment        | 30         |
| Integration                | 10         |
| **Participation Bonus**    | 50         |

---

## **Submission Guidelines**
1. Push your code to a GitHub repository.  
2. Ensure each part is saved with the specified file names.  
3. Include a `submission.md` file with your team name and any additional notes.  

---

## **Tips & Extra Credit**
- Try advanced techniques to improve object detection and lane detection performance.  
- Successfully deploy an improved model on TensorRT to earn extra points.  

Good luck, and may the best team win! 🚀
