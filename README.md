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


# Standard results format
For every single model deployed in every single NPU, the Data shown below should be collected:

| **Number** | **Type**                                                                  | **Value** |
|------------|---------------------------------------------------------------------------|-----------|
| 1          | pth Accuracy (%) of full precision model                                  |           |
| 2          | onnx Accuracy (%) of full precision model                                 |           |
| 3          | onnx Accuracy (%) of full quantized model (e.g., w8a8)                    |           |
| 4          | onnx Accuracy (%) of mixed quantization model by our quantizing framework |           |
| 5          | onnx Accuracy (%) of AMCT-like addressed  model from 4                    |           |
| 6          | Accuracy (%) of om-like addressed model from 5                            |           |
| 7          | Latency (ms) of om-like-formatted model from 2                            |           |
| 8          | Latency (ms) of om-like-formatted model from 3                            |           |
| 9          | Latency (ms) of om-like-formatted model from 5                            |           |
| oa1        | maximal accuracy (%) drop                                                 |           |
| oa2        | accuracy (%) drop of ours                                                 |           |
| os1        | maximal speedup                                                           |           |
| os2        | speedup (%) of ours                                                       |           |




# Progress

[20250212] Probably matched. For YOLOv10s, mAP (%) is 46.2 (tested with pth format and ultralytics), 44.34 (tested with onnx format and our code) 44.17 (tested after through our quantization method) 44.12 (tested after through AMCT).



# Significant bugs

**[2025021001]** Activation quantization as well leads to misaligned scales in the second quantization.

[2025021101] The overly long generation time of onnx files of quantized YOLOv10.


# Potentially valuable scientific issues

1. Whether to quantize a CNN before or after BN fusion.

2. Is the present method already proper for across architectures and tasks? 

3. Slow mixed precision quantizatin scheme generation time. 
