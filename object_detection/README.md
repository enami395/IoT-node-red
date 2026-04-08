# Object Detection with Node-RED (TensorFlow)

## Objective

Build a simple IoT application that detects objects in images using TensorFlow inside Node-RED.

## Technologies

* Node-RED
* TensorFlow (COCO-SSD)
* Node-RED Dashboard

## 📥 Flow Description

The flow performs:

1. Image upload from dashboard
2. Conversion (base64 → buffer)
3. Object detection using COCO-SSD
4. Display of detected objects and confidence score

## How to Run

1. Install dependencies:

   ```
   npm install node-red-contrib-tensorflow
   ```
2. Import `flow.json` into Node-RED
3. Deploy the flow
4. Open the dashboard and upload an image

## Output

* Detected object label
* Image preview
