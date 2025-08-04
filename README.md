# Trash Detector

This project uses a custom-trained Trashnet model to classify waste from a live camera. Based on the prediction, it recommends the correct recycling bin: landfill, paper/cardboard, or bottles/cans. The system is designed for interactive use and promotes smarter, sustainable waste sorting.

![Screenshot of what running and using the project looks like](https://github.com/user-attachments/assets/99fd6f1b-dc85-4429-93c4-88cde33b9805)

## The Algorithm

The model is a ResNet-18 trained to distinguish between: cardboard, paper, plastic, metal, glass, and trash. It's exported as an ONNX file along with a label file. The system uses a live video feed and waits for the user to press Enter. It then captures a image from the video feed and runs the model on the image. It will then tell the user the predicted class and confidence and tell the user which bin to put it in.

## Running this project

To run the project, follow these steps:
1. Install these required libraries: numpy, Pillow, onnx, jetson-inference, jetson-utils
2. cd into ~/jetson-inference/python/training/classification
3. Run `python3 trash_predictor.py`
4. Put a piece of trash underneath the camera and click enter to classify
5. Then throw the trash away in the right bin

[View a video explanation here](https://drive.google.com/file/d/1UHNK6GOIFCyZuPFm-b7mDBqEtxLwtmn8/view?usp=sharing)
https://github.com/user-attachments/assets/1e76b9f4-0711-4436-8b32-68788e81e0c1
