

# Init


```bash
pip install -r requirements-gpu-dev.txt
```

+ `PytorchStreamReader failed reading zip archive: failed finding central directory`

  redownload model

+ `ImportError: DLL load failed while importing onnx_cpp2py_export`

  https://github.com/CVHub520/X-AnyLabeling/issues/564

+ `Error in loading model: open_vision with error: OpenVision model will not be available. Please install related packages and try again.`

  https://github.com/CVHub520/X-AnyLabeling/issues/737



# Model

+ DAMO-YOLO：https://github.com/tinyvision/DAMO-YOLO?tab=readme-ov-file

  | Model                                                        | size | mAPval 0.5:0.95 | Latency T4 TRT-FP16-BS1 | FLOPs (G) | Params (M) | AliYun Download                                              | Google Download |
  | ------------------------------------------------------------ | ---- | --------------- | ----------------------- | --------- | ---------- | ------------------------------------------------------------ | --------------- |
  | [DAMO-YOLO-T](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL20_T.py) | 640  | 42.0            | 2.78                    | 18.1      | 8.5        | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL20_T_420.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL20_T_420.onnx) | --              |
  | [DAMO-YOLO-T*](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL20_T.py) | 640  | 43.6            | 2.78                    | 18.1      | 8.5        | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL20_T_436.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL20_T_436.onnx) | --              |
  | [DAMO-YOLO-S](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL25_S.py) | 640  | 46.0            | 3.83                    | 37.8      | 16.3       | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL25_S_460.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL25_S_460.onnx) | --              |
  | [DAMO-YOLO-S*](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL25_S.py) | 640  | 47.7            | 3.83                    | 37.8      | 16.3       | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL25_S_477.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL25_S_477.onnx) | --              |
  | [DAMO-YOLO-M](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL35_M.py) | 640  | 49.2            | 5.62                    | 61.8      | 28.2       | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL35_M_492.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL35_M_492.onnx) | --              |
  | [DAMO-YOLO-M*](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL35_M.py) | 640  | 50.2            | 5.62                    | 61.8      | 28.2       | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL35_M_502.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL35_M_502.onnx) | --              |
  | [DAMO-YOLO-L](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL45_L.py) | 640  | 50.8            | 7.95                    | 97.3      | 42.1       | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL45_L_508.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL45_L_508.onnx) | --              |
  | [DAMO-YOLO-L*](https://github.com/tinyvision/DAMO-YOLO/blob/master/configs/damoyolo_tinynasL45_L.py) | 640  | 51.9            | 7.95                    | 97.3      | 42.1       | [torch](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/clean_model_0317/damoyolo_tinynasL45_L_519.pth),[onnx](https://idstcv.oss-cn-zhangjiakou.aliyuncs.com/DAMO-YOLO/release_model/onnx/damoyolo_tinynasL45_L_519.onnx) | --              |

+ GROUNDING-DINO：https://github.com/IDEA-Research/GroundingDINO?tab=readme-ov-file

  | name | backbone        | Data   | box AP on COCO                                   | Checkpoint                          | Config                                                       |                                                              |
  | ---- | --------------- | ------ | ------------------------------------------------ | ----------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
  | 1    | GroundingDINO-T | Swin-T | O365,GoldG,Cap4M                                 | 48.4 (zero-shot) / 57.2 (fine-tune) | [GitHub link](https://github.com/IDEA-Research/GroundingDINO/releases/download/v0.1.0-alpha/groundingdino_swint_ogc.pth) \| [HF link](https://huggingface.co/ShilongLiu/GroundingDINO/resolve/main/groundingdino_swint_ogc.pth) | [link](https://github.com/IDEA-Research/GroundingDINO/blob/main/groundingdino/config/GroundingDINO_SwinT_OGC.py) |
  | 2    | GroundingDINO-B | Swin-B | COCO,O365,GoldG,Cap4M,OpenImage,ODinW-35,RefCOCO | 56.7                                | [GitHub link](https://github.com/IDEA-Research/GroundingDINO/releases/download/v0.1.0-alpha2/groundingdino_swinb_cogcoor.pth) \| [HF link](https://huggingface.co/ShilongLiu/GroundingDINO/resolve/main/groundingdino_swinb_cogcoor.pth) | [link](https://github.com/IDEA-Research/GroundingDINO/blob/main/groundingdino/config/GroundingDINO_SwinB_cfg.py) |

+ GOLD-YOLO：https://zhuanlan.zhihu.com/p/657742732

  | Model       | Size | Self-Distill | Pre-Train Backbone | mAPval 0.5:0.95 | Speed (fps) T4-TRT7-FP16 bs1 / bs32 | Speed (fps) T4-TRT8-FP16 bs1 / bs32 | Params (M) | FLOPs (G) | Weight                                                       |
  | ----------- | ---- | ------------ | ------------------ | --------------- | ----------------------------------- | ----------------------------------- | ---------- | --------- | ------------------------------------------------------------ |
  | Gold-YOLO-N | 640  | ✅            | ❌                  | 39.9            | 563 / 1030                          | 657 / 1191                          | 5.6        | 12.1      | [Google Drive](https://drive.google.com/drive/folders/1dd2KJjYfHrXwKasfjDeL1eLX0Vp6UaLG) [cowtransfer](https://traly.cowtransfer.com/s/9cd33702ca404f) |
  | Gold-YOLO-S | 640  | ✅            | ✅                  | 46.4            | 286 / 446                           | 308 / 492                           | 21.5       | 46.0      | [Google Drive](https://drive.google.com/drive/folders/1dd2KJjYfHrXwKasfjDeL1eLX0Vp6UaLG) [cowtransfer](https://traly.cowtransfer.com/s/9cd33702ca404f) |
  | Gold-YOLO-M | 640  | ✅            | ✅                  | 51.1            | 152 / 220                           | 157 / 241                           | 41.3       | 87.5      | [Google Drive](https://drive.google.com/drive/folders/1dd2KJjYfHrXwKasfjDeL1eLX0Vp6UaLG) [cowtransfer](https://traly.cowtransfer.com/s/9cd33702ca404f) |
  | Gold-YOLO-L | 640  | ✅            | ✅                  | 53.3            | 88 / 116                            | 94 / 137                            | 75.1       | 151.7     | [Google Drive](https://drive.google.com/drive/folders/1dd2KJjYfHrXwKasfjDeL1eLX0Vp6UaLG) [cowtransfer](https://traly.cowtransfer.com/s/9cd33702ca404f) |

+ YOLO-NAS：https://github.com/Deci-AI/super-gradients/blob/master/YOLONAS.md

  | Model            | mAP   | Latency (ms) |
  | ---------------- | ----- | ------------ |
  | YOLO-NAS S       | 47.5  | 3.21         |
  | YOLO-NAS M       | 51.55 | 5.85         |
  | YOLO-NAS L       | 52.22 | 7.87         |
  | YOLO-NAS S INT-8 | 47.03 | 2.36         |
  | YOLO-NAS M INT-8 | 51.0  | 3.78         |
  | YOLO-NAS L INT-8 | 52.1  | 4.78         |