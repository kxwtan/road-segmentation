# road-segmentation

This notebook uses a [UNet](https://arxiv.org/pdf/1505.04597v1) architecture for semantic segmentation. It consists of two processes: downsampling and upsampling. Downsampling involves a repeated application of the following sequence: 3x3 convolution layer, ReLU activation function, and 2x2 max-pooling; where at each repetition, the number of feature channels is doubled. Afterwards, upsampling is applied in which it applies an "up-convolution" that halves the number of feature channels, followed by a repeated application of 3x3 convolution and ReLU. In the code, Batch Normalization and Dropout was added to ensure better performance and accuracy.

Below is some comparisons between the model's performance and the actual expected segmentation:
![Screenshot 2024-05-07 at 10 12 16 PM](https://github.com/kxwtan/road-segmentation/assets/58784851/5f5aa8b1-fb7a-43f6-b748-8ec0d0e81a2a)

