---
title: Getting Started
icon: fas fa-play
order: 2
---

Welcome to EZ-FRCNN! This tool is designed to make machine learning more accessible, helping you to use advanced image detection without needing a deep background in programming or machine learning. Below, you’ll find simple steps to get started with annotation, training, and inference.

## Step 1: Annotation – Labeling Your Images

Annotation is the process of labeling the objects in your images that you want the model to recognize. This might include specific structures, organisms, or other items you’re interested in identifying.

1. **Select Images to Annotate**: Before opening the app, place all images you would like to annotate to the "annotations" folder.
2. **Select Your Classes**: After opening the annotation app, choose the classes (category) you want to annotate. For example, if you’re labeling cells, you might have classes like “nucleus” or “cell membrane.”
3. **Draw Bounding Boxes**: With your class selected, draw a box around each object in the image that belongs to that class. Repeat this step for each class you want the model to learn.
4. **Save Your Annotations**: Once all objects in an image are labeled, save your annotations. You’ll repeat these steps for a few images to give the model enough examples to learn from.

> **Tip**: Annotation can take a bit of time, but the more images you label, the better your model will perform. Aim for at least 20-50 labeled images to get started.

## Step 2: Training – Teaching the Model to Recognize Your Objects

Once your images are annotated, you’re ready to train the model. Training is where the model learns to recognize your labeled objects based on the examples you provided.

1. **Training and Validation Sets**: During training, your data is split into two sets:
   - **Training Set**: This set is used to teach the model how to recognize your objects.
   - **Validation Set**: This set checks the model’s learning progress on new images it hasn’t seen, helping to ensure it’s generalizing rather than memorizing.
   
   Both sets are crucial: the training set helps the model learn, while the validation set ensures that learning applies to new images.

2. **Understanding the Loss Curves**: During training, you’ll see two curves— **training loss** and **validation loss**. These curves represent how well the model is performing:
   - **Training Loss**: Shows how well the model is learning on the images it’s trained on.
   - **Validation Loss**: Indicates how well the model generalizes to new, unseen images.
   
   Ideally, both curves will decrease over time. If validation loss stops decreasing or begins to rise, it can mean the model is overfitting (learning too specifically to the training data), which may require more varied data or adjustments.

3. **Finish Training**: Once the model completes training, it will be ready to use. 

> **Tip**: If you have a larger set of annotated images, the model can learn more accurately, but training might take longer. Start with a small set, and as you grow comfortable, you can add more images and retrain.

## Step 3: Inference – Using the Model to Detect Objects in New Images

Inference is when the trained model applies what it’s learned to new, unlabeled images. Here, the model will identify and label objects on its own based on the patterns it learned during training.

1. **Select New Images**: Place new images where you want the model to detect objects automatically into "test_data/test_images".
2. **Run Inference**: Select the "Run Inference" option in EZ-FRCNN. The model will process your images and label objects based on your training.
3. **Review the Results**: After inference completes, you’ll see boxes around the detected objects in your images, along with confidence scores. 

   - **Confidence Score**: This number (from 0 to 1) shows the model’s certainty about each detection, where higher scores mean greater confidence in the label.
   
4. **CSV Output**: The tool also generates a CSV file listing each image name, detected object, and the confidence score. This provides a quick overview and easy access to results for further analysis.

> **Tip**: If the results aren’t as accurate as you’d like, consider adding more annotations and retraining the model.

## Additional Tips for Success

- **Start Small**: Begin with a small number of images and labels. As you gain experience, you can add more data to improve accuracy.
- **Use Clear Images**: The clearer and higher-quality your images, the better your model will perform.
- **Iterate**: Machine learning models improve with iteration. Each round of annotation, training, and inference makes the model a little better!

EZ-FRCNN was built to make machine learning accessible and user-friendly. Follow these steps, experiment, and soon you’ll have a trained model that recognizes your objects of interest with minimal effort!
