├── dataset/
│   ├── frames/                # Directory for storing extracted frames from videos
│   │   ├── train/             # Training video frames
│   │   │   ├── video1_frames (推荐 30fps)/
│   │   │   │   ├── frame1.jpg
│   │   │   │   ├── frame2.jpg
│   │   │   │   └── ...
│   │   │   ├── video2_frames/
│   │   │   │   ├── frame1.jpg
│   │   │   │   ├── frame2.jpg
│   │   │   │   └── ...
│   │   ├── val/               # Validation video frames
│   │   │   ├── video3_frames/
│   │   │   │   ├── frame1.jpg
│   │   │   │   ├── frame2.jpg
│   │   │   │   └── ...
│   │   │   ├── video4_frames/
│   │   │   │   ├── frame1.jpg
│   │   │   │   ├── frame2.jpg
│   │   │   │   └── ...
│   │   └── test/              # Test video frames (optional)
│   │       ├── video5_frames/
│   │       │   ├── frame1.jpg
│   │       │   ├── frame2.jpg
│   │       │   └── ...
│   ├── labels/                # Directory for storing YOLO annotations
│   │   ├── train/             # YOLO annotations for training video frames
│   │   │   ├── video1_frames/
│   │   │   │   ├── frame1.txt
│   │   │   │   ├── frame2.txt
│   │   │   │   └── ...
│   │   │   ├── video2_frames/
│   │   │   │   ├── frame1.txt
│   │   │   │   ├── frame2.txt
│   │   │   │   └── ...
│   │   ├── val/               # YOLO annotations for validation video frames
│   │   │   ├── video3_frames/
│   │   │   │   ├── frame1.txt
│   │   │   │   ├── frame2.txt
│   │   │   │   └── ...
│   │   │   ├── video4_frames/
│   │   │   │   ├── frame1.txt
│   │   │   │   ├── frame2.txt
│   │   │   │   └── ...
│   │   └── test/              # YOLO annotations for test video frames (optional)
│   │       ├── video5_frames/
│   │       │   ├── frame1.txt
│   │       │   ├── frame2.txt
│   │       │   └── ...
└── dataset.yaml               # Dataset configuration file (YAML)