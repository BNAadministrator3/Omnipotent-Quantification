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


# Potentially valuable scientific issues

1. Whether to quantize a CNN before or after BN fusion.

2. Is the present method already proper for across architectures and tasks? 

3. Slow mixed precision quantizatin scheme generation time. 
