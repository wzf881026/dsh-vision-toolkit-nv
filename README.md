# dsh-vision-toolkit-nv model assets

Hosts model files for the `dsh-vision-toolkit-nv` DSH vision plugin. The plugin
itself is distributed through its npm package; this repository only serves
release assets so `scripts/fetch-models.mjs` can download them.

## Assets

### `models-v1`

- `yolox_s.onnx` — YOLOX-s exported to ONNX for the plugin's `nv_vision_detect`
  tool.
  - Input: `[1, 3, 640, 640]` float32 BGR, 0-255
  - Output: `[1, 8400, 85]` (xywh + objectness + 80 COCO scores, decoded)
  - Opset: 11
  - Bytes: 35,972,353
  - SHA-256: `86c98f2ce49c9430eb73d807490afcfe8ae84d7f3a3b2170e47e71e20a249d85`
  - License: Apache-2.0 (YOLOX, Megvii-BaseDetection), exported from the
    official `yolox_s.pth` release with `scripts/export-yolox-onnx.py`
  - Upstream: https://github.com/Megvii-BaseDetection/YOLOX

Ultralytics / YOLOv8 weights are not hosted here: they are AGPL-3.0 and are
deliberately excluded from the plugin.
