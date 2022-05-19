# Image classification project

The project will classify various imaging images such as Xray and colonoscopy by transfer learning.

As part of the project, a quality CNN network was developed, that includes:

• Augmentation

• Several stages of training

• Monitoring of training.

• Optimization of hyper parameters.

• Execution of Classifier based on features from the network.

### DATA:

The data contain 3 types of chest x-ray

1- Chest X-Rays in Patients with COVID-19  (Winner of the COVID-19 Dataset Award by Kaggle Community)

COVID-19 (coronavirus disease 2019) is an illness caused by a virus. This virus is a coronavirus called SARS-CoV-2. It spreads when a person who has the infection breathes out droplets and very small particles that contain the virus.

2- Chest X-Rays in Patients with Pneumonia

Pneumonia is an infection in one or both of the lungs. It causes the air sacs of the lungs to fill up with fluid or pus. It can range from mild to severe, depending on the type of germ causing the infection, your age, and your overall health.

3- Normal Chest X-Rays

### ResNet-50 Model:
ResNet-50 is a convolutional neural network that is 50 layers deep. ResNet, short for Residual Networks. The resnet 50 architecture contains the following element:

1.	A convoultion with a kernel size of 7 * 7 and 64 different kernels all with a stride of size 2 giving us 1 layer.
2.	Next we see max pooling with also a stride size of 2.
3.	In the next convolution there is a 1 * 1,64 kernel following this a 3 * 3,64 kernel and at last a 1 * 1,256 kernel, These three layers are repeated in total 3 time so giving us 9 layers in this step.
4.	Next we see kernel of 1 * 1,128 after that a kernel of 3 * 3,128 and at last a kernel of 1 * 1,512 this step was repeated 4 time so giving us 12 layers in this step.
5.	After that there is a kernal of 1 * 1,256 and two more kernels with 3 * 3,256 and 1 * 1,1024 and this is repeated 6 time giving us a total of 18 layers.
6.	And then again a 1 * 1,512 kernel with two more of 3 * 3,512 and 1 * 1,2048 and this was repeated 3 times giving us a total of 9 layers.
7.	After that we do a average pool and end it with a fully connected layer containing 1000 nodes and at the end a softmax function so this gives us 1 layer.


We don't actually count the activation functions and the max/ average pooling layers.

so totaling this it gives us a 1 + 9 + 12 + 18 + 9 + 1 = 50 layers Deep Convolutional network.

Found 13953 images belonging to 3 classes.
Found 600 images belonging to 3 classes.
Found 600 images belonging to 3 classes.

trian size COVID 3216
trian size Normal 9792
trian size Viral Pneumonia 945

test size COVID  200
test size large  200
test size Viral Pneumonia  200

### results:

The results is reported as the accuracy of each classifier, using the following metrics when these are applicable:

• precision

• recall

• F1-score

• Accuracy

• Plot
