# Omnipotent-Quantification
This repo integrates our quantization method that enables highly accurate and efficient mixed-precision quantization across different network architectures, tasks, and NPUs.

# Objectives and key results
Hopefully, our proposed quantization method:

**01**. supports quantization for different network architectures

**K1**. YOLOv10, DINO or H-DETR.

**02**. supports quantization for different tasks

**K2**. object detection, segmentation or/and image generation.

**03**. supports quantization for different types of NPUs

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
| 7          | Accuracy (%) of om-like addressed model from 2                            |           |
| 8          | Accuracy (%) of om-like addressed model from 3                            |           |
| 9          | Latency (ms) of om-like-formatted model from 5                            |           |
| 10          | Latency (ms) of om-like-formatted model from 2                            |           |
| 11          | Latency (ms) of om-like-formatted model from 3                            |           |
| o0       | diff(4,5)<0.1%    |  True/False  |
| oa1        | maximal simulated accuracy (%) drop, i.e., diff(2, 4)                                                |           |
| oa2        | simulated accuracy (%) drop of ours, i.e., diff(2, 3)                                                 |           |
| oa3        | maximal practical accuracy (%) drop, i.e., diff(7, 8)                                                |           |
| oa4        | practical accuracy (%) drop of ours, i.e., diff(7, 6)                                                 |           |
| os1        | maximal speedup, i.e., div(10, 9)                                                           |           |
| os2        | speedup (%) of ours, i.e., div(10,11)                                                       |           |




# Progress

[20250212] Probably matched. For YOLOv10s, mAP (%) is 46.2 (tested with pth format and ultralytics), 44.34 (tested with onnx format and our code) 44.17 (tested after through our quantization method) 44.12 (tested after through AMCT).


# Some know-how

1. We suppose AOE optimization should also be integrated into our method. 


# Significant bugs

**[2025021001]** Activation quantization as well leads to misaligned scales in the second quantization.

[2025021101] The overly long generation time of onnx files of quantized YOLOv10.


# Potentially valuable scientific issues

1. Whether to quantize a CNN before or after BN fusion.

2. Is the present method already proper for across architectures and tasks? 

3. Slow mixed precision quantization scheme generation time. 
