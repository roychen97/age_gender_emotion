# age_gender_emotion

Feature extraction model is a modified version of mobilenetv3, and use the extracted features on 3 functions:
1. regression for age of the face
2. classify for gender of the face
3. classify for emotion of the face

Because the features used in these functions are highly overlapped, 1 backbone model for all of them can reduce alot of model size and time cost to inference.

The testing result showed that, after I increased the channel count of the single backbone model to 1.5x, the accuracy is on par with inplementing each of the funtions seperately with their own backbone model.

also include the code to freeze the model to a pb file for inferencing
