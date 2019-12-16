# Facial-Features-Detection
Facial Features Detection
In this project the concept of transfer learning is used which means using the knowledge gained while solving one problem and applying it on a different related problem.
So i used the knowledge gained by the model facenet_keras.h5(which encodes the given image into 128x1 dimension) to detect the facial features/keypoints.
specification of facenet_keras.h5 model :
                                        input shape : (160x160x3)
                                        output shape : (128x1)
                                        purpose : to encode the given image into 128x1 dimension 
changes made to the above model while keeping the weights same:
                                        input shape : (200x200x3)
                                        output shape: (388,1) ((x,y) coordinates of 194 keypoints)
                                        purpose : to detect facial features/keypoints
 
