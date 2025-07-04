Report on Data Augmentation

Techniques Applied
Rotation: Random rotations up to 30 degrees
Zoom: 0.2 range zoom-in/out
Width & Height Shift: Small shifts to simulate real-world variation
Horizontal & Vertical Flip: To simulate mirrored leaf appearance
Rescale: Pixel normalization using rescale=1./255
Brightness: between 0.8 to 1.2 Range
Effectiveness
Helped reduce overfitting in the Custom CNN model
Did not significantly improve transfer learning models due to limited data
Conclusion
While Transfer Learning models did not outperform the Custom CNN due to the extremely limited dataset size (~120 images), data augmentation played a vital role in improving the generalizability of the custom architecture.

Report on Models

Custom CNN Model
Structure: 3 convolutional layers with increasing filter depth, followed by max pooling, flattening, and dense layers.
Loss Function: Sparse Categorical Crossentropy
Accuracy: ~83% (best performance among all models tested)
Performed decently with limited data; susceptible to overfitting. Reduced complexity helped improve generalization.

MobileNetV2
Transfer Learning: Used pretrained weights from ImageNet; only last few layers unfrozen.
Used Because Lightweight, fast inference, efficient on small datasets.
Accuracy: ~33%
Failed to generalize due to small dataset size and limited variation.

ResNet50
Transfer Learning: Pretrained on ImageNet, final layers customized.
Reason for Used: Deep architecture good for learning complex patterns.
Accuracy: ~33%
Suffered from underfitting; not suitable for extremely small datasets without further tuning.

EfficientNetB0
Transfer Learning: Pretrained backbone, Global Average Pooling, and Dense output.
Why Used: Balanced in terms of parameters and accuracy.
Accuracy: ~33%
Could not leverage full potential due to insufficient data.
