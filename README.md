# MobileNet_PlantZombie
Model File:
plant_disease_model_fp16.tflite

Framework: TensorFlow Lite
Backbone: MobileNetV2
Task: Image classification (plant disease detection)

# Input Specification
- Input shape: (1, 160, 160, 3)
- Data type: float32
- Pixel range: 0 – 255
- Color format: RGB
- Batch size: 1

# Output Specification
- Output shape: (1, num_classes)
- Data type: float32
- Output là probability distribution

  # Getting results
  val predictedClass = outputArray[0].indices.maxBy { outputArray[0][it] }

# Labels Mapping

labels.txt

Format:

0 Apple___Apple_scab
1 Apple___Black_rot
2 Apple___Cedar_apple_rust
...

- Map:

predicted_index → labels[predicted_index]

- Files Included
plant_disease_model_fp16.tflite ( 16 bit quantized )
plant_disease_model.tflite ( 32 bit quantized )
labels.txt
README.md
best_model.keras (for retraining only)
