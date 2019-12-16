# Facial-Features-Detection-From-Scratch
Facial Features Detection

In this project the concept of transfer learning is used which is using the knowledge gained while solving one problem and applying it on a different related problem.

So i used the knowledge gained by the model facenet_keras.h5(which encodes the given image into 128x1 dimension) to detect the facial features/keypoints.

specification of facenet_keras.h5 model :

                                        input shape : (160x160x3)
                                        output shape : (128x1)
                                        purpose : to encode the given image into 128x1 dimension 
                                        
changes made to the above model while keeping the weights same:

                                        input shape : (200x200x3)
                                        output shape: (388,1) ((x,y) coordinates of 194 keypoints)
                                        purpose : to detect facial features/keypoints
                                     
The layers with name block8,avgpool,Dropout were only allowed to train while the weights of other layer were kept same.

The model was then trained on the HELEN DATASET- http://www.ifp.illinois.edu/~vuongle2/helen/

For training the model:
                        
                         training data size: 2000 images (all were converted to numpy array(img.npy))
                         optimizer used : Adam Optimizer
                         Learning Rate: 0.0001
                         Loss function: mean_squared_error
                         No of epochs: 500
                         batch_size: 32
                         results:can be seen in the provided result folder.
 THE TRAINED MODEL IS ALSO PROVIDED.
