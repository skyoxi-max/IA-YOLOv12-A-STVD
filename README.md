IA-YOLOv12-A-STVD/
│
├── README.md                      <-- Main landing page with detailed setup & documentation
├── LICENSE                        <-- Open-source license (e.g., MIT or Apache 2.0)
├── requirements.txt               <-- Python dependencies & package versions
├── environment.yaml               <-- Conda environment export file
│
├── data/                          <-- Data guidelines & annotations
│   ├── README.md                  <-- Instructions on downloading public datasets & accessing D_Local
│   ├── taxonomy_mapping.json      <-- MSeg categorical semantic mapping rules (COCO/IDD/Cityscapes -> Unified)
│   └── custom_bhilai_sample/      <-- Sample subset of Bhilai annotated images (CVAT XML/YOLO format)
│
├── modules/                       <-- Core Python research code
│   ├── __init__.py
│   ├── ia_dip.py                  <-- Algorithm 1: Image-Adaptive DIP & Radiometric Restoration
│   ├── yolo_gca.py                <-- Algorithm 2: IA-YOLOv12 Backbone with Global Contextual Attention
│   ├── mseg_unification.py        <-- Algorithm 3: Information-Theoretic Taxonomic Gating & Mapping
│   └── astvd_tracking.py          <-- Algorithm 4: Kalman Filtering & Mahalanobis Distance Violation Logic
│
├── scripts/                       <-- Training and Evaluation Scripts
│   ├── train.py                   <-- Algorithm A: Multi-dataset preparation & model training pipeline
│   ├── evaluate.py                <-- mAP, Precision, Recall, F1, and AUC metric calculation
│   ├── infer_edge.py              <-- Hailo-8 / Raspberry Pi 5 INT8 quantized edge inference runner
│   └── simulate_noise_jitter.py   <-- Synthetic dark-box (20 Lux) and kinematic jitter test generation
│
└── weights/                       <-- Model checkpoint links / files
    └── README.md                  <-- Direct links to trained FP32 and INT8 ONNX/HEF model weights
