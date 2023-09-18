# RD-Data-Takehome-Sagarika-Ramesh
REAL AND FAKE FACE DETECTOR

Deep Learning Classifier used for the classification:
1)VGG model - transfer learning(for feature extraction)
2)CNN model
3)VGGFace - transfer learning(for feature extraction)
All these models are train on fewer epochs and small dataset. The performance of these models can be increased with fine tuning the model (by adding more layers, Hyperparameter Tuning, Regularization..etc )

Dataset information:
Real images are obtained from Flickr. (Flickr-Faces-HQ (FFHQ)). 1082 random images are selected. Fake images are obtained from A Style-Based Generator Architecture for Generative Adversarial Networks created by Tero Karras (NVIDIA), Samuli Laine (NVIDIA), Timo Aila (NVIDIA). It is made publicly available for research purposes. 961 random images are selected. The data set is not imbalanced. There is no bias as the dataset contains people from different regions, race, age, gender and pose
Data for Test(Unseen Data): For test set, I have collected data from seperate source to avoid data leakage. Data is obtained from Computational Intelligence and Photography Lab,Department of Computer Science, Yonsei University. The data is expert-generated high-quality photoshopped face images. These images are not obtained from GAN.

Method2 for dataset creation:(This method did not work - requires more time) I have chosen to use CelebA data. Firstly, I wanted a data set that is publicly accessible to everyone. CelebA data contains 200,000+ images of celebrity faces and it includes diversity with people belonging to different races, genders,and ages. This data can be used as Real face Images. Fake Face images are then created using DCGAN(Deep Convolutional Generative Adversarial Network). I tried to generate fake face images using this method but it was very time consuming to train the model and generate a deep fake face image. Data set was downloaded from http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html website. I select random 400 images from that dataset to create celeb_face_real dataset. DCGA(Deep convolutional generative Adversarial network)was used to generate fake face images from the real face images. 80 epochs are run and the images generated after each epoch are stored in celeb_face_fake folder.


