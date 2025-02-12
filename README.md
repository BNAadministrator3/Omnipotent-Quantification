# Omnipotent-Quantification
This repo integrates our quantization method that enables highly accurate and efficient quantization across different network architectures, tasks, and NPUs.

# Objectives and key results
Hopefully, our proposed quantization method:

**01**. supports quantizatin for different network architectures

**K1**. YOLOv10, DINO or H-DETR.

**02**. supports quantizatin for different tasks

**K2**. object detection, segmentation or/and image generation.

**03**. supports quantizatin for different types of NPUs

**K3**. Ascend 310b1, Ascend 310b4, Cambrian, Rockchip.

**04**. possesses high efficiency.

**K4**. cost model?


# Progress

[20250212] Probably matched. For YOLOv10s, mAP (%) is 46.2 (tested with pth format and ultralytics), 44.34 (tested with onnx format and our code) 44.17 (tested after through our quantization method) 44.12 (tested after through AMCT).



# Significant bugs

**[2025021001]** Activation quantization as well leads to misaligned scales in the second quantization.

[2025021101] The overly long generation time of onnx files of quantized YOLOv10.


# Potentially valuable scientific issues

1. Whether to quantize a CNN before or after BN fusion.

2. Is the present method already proper for across architectures and tasks? 

3. Slow mixed precision quantizatin scheme generation time. 
