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
