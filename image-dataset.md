# Image Dataset Structure Overview

├── trafic_data/
│   ├── images/               # Directory for storing images
│   │   ├── train/            # Training images
│   │   │   ├── image1.jpg
│   │   │   ├── image2.jpg
│   │   │   └── ...
│   │   ├── valid/              # Validation images
│   │   │   ├── image3.jpg
│   │   │   ├── image4.jpg
│   │   │   └── ...
│   ├── labels/               # Directory for storing annotations
│   │   ├── train/            # YOLO annotations for training images
│   │   │   ├── image1.txt
│   │   │   ├── image2.txt
│   │   │   └── ...
│   │   ├── valid/              # YOLO annotations for validation images
│   │   │   ├── image3.txt
│   │   │   ├── image4.txt
│   │   │   └── ...
└── data_1.yaml             # Dataset configuration file (YAML)