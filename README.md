Face recognition, which is becoming widespread and gaining importance gradually,  is one of the application areas of artificial intelligence. Face recognition systems are used in many places from public institutions to private organizations. However, due to pandemic, Covid 19, people wear masks and masked-face may not be recognized by current face recognition models. In this paper, I will investigate whether current face recognition models are successful to recognize masked-face or not. 
My other works : 
1)  [For Face Recognition with FaceNet Encoding model with RMFRD](https://www.kaggle.com/muhammeddalkran/masked-unmasked-face-recogniti), \n
[For Face Recognition with FaceNet Encoding model with SMFRD](https://www.kaggle.com/muhammeddalkran/face-recognition-with-lfw-smfrd),
[For Face Recognition with FaceNet Embedding and SVC’s Linear Kernel model with  RMFRD](https://www.kaggle.com/muhammeddalkran/masked-face-recognition-with-rmfrd), 
[For Face Recognition with FaceNet Embedding and SVC’s Linear Kernel model with SMFRD](https://www.kaggle.com/muhammeddalkran/masked-face-recognition-with-lfw-smfrd
).

# Face Recognition with DeepFace Ensemble Learning
  The model is open source model; source code and GitHub page [link](https://github.com/serengil/deepface). The pipeline of the model is: Face Detection, Face Alignment, Face Representation, and Face Verification. I will explain each part of the pipeline below. 
## Face Detection 
  The first part of the pipeline is face detection. To detect faces, the model utilizes a neural network called ResNet Single Shot-Multibox Detector (SSD) with OpenCV library. The basis of the ResNet SSD is VGG which will be explained later. 
## Face Alignment
  The second part of the pipeline is face alignment. To align faces, [OpenCV’s haar cascade](https://github.com/opencv/opencv/tree/master/data/haarcascades) method is used. Haar cascade method can be used to align eyes and frontal face. Haar cascade can process 6.50 frames per second.
## Face representation
  The third part of the pipeline is to create face representation. In this part, the model utilizes different models since it is a product of ensemble learning. The representation models used by models are VGG-Face, Google FaceNet, OpenFace, Facebook DeepFace. Addition to differences in the performance of the model, the required input size, output size, and vector structure of the output are differences among representation models. 
## Face Verification
  The last part of the pipeline is to verify and identify faces. Until this part, representation of the face, namely face features’ vectors, are created. In this part, faces are verified and identified  by using distance metrics which are cosine, euclidean, and euclidean L2. The euclidean distance was explained in part 2.1, please look at this section. I will explain cosine similarity metric. According to the distance and similarity metric results, the face(s) is identified and the model indicates whose face in the dataset, database or input data, is closer to the given face. 

