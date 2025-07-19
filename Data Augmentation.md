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
