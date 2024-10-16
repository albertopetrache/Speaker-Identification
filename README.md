# Speaker Identification
In this project, I investigated the performance of various speaker identification methods
using the Librispeech and TIMIT datasets. My methodologies included the use of fully
connected neural networks (FCNN) and convolutional neural networks (CNN), extracting
a wide range of features from audio signals such as mel‐frequency cepstral coefficients
(MFCC), delta and delta‐delta MFCCs, linear predictive coding (LPC) coefficients, and
spectrograms. I also explored the effectiveness of pre‐trained models such as
“squeezenet1_0”, “densenet121”, and “vgg16”.

In this project, I used three approaches to analyze audio signals, each employing different neural network architectures for speaker identification.
I. Approach based on Fully Connected Neural Networks (FCNN): I selected a set of significant features for the representation and analysis of the audio signal: MFCC (Mel-frequency cepstral coefficients), delta and delta-delta MFCC, LPC coefficients, and the zero-crossing rate. After feature extraction, I concatenated these features to form a final feature vector, and then calculated the mean and standard deviation for each feature across the entire resulting vector. These statistics were then concatenated to form a final feature vector at the recording level.

II. Approach based on Convolutional Neural Networks (CNN): In this approach based on convolutional neural networks, I used spectrograms generated from audio recordings to train a CNN model for speaker identification. Given the variation in the length of audio recordings in the Librispeech and TIMIT datasets, I calculated the maximum length of a recording from both datasets. To standardize the dimensions, I padded the recordings with zero-value samples up to the calculated maximum length.

III. Approach based on the use of pre-trained networks: In this approach, I utilized pre-trained models such as SqueezeNet, DenseNet, and VGG as backbones for processing audio spectrograms. After selecting a pre-trained neural network and removing the final classification layer, I extended the architecture by adding additional layers to adjust the learning process for the classification of the spectrograms.












