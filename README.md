# Virtual-IHC-Generation
This project aims to directly generate immunohistochemistry(IHC) stained WSIs from HE-stained WSIs to assess immunohistochemical expression using CycleGAN.

## Usage Instructions

1. **Preprocessing**  
   First, perform image registration between the two types of stained Whole Slide Images (WSIs).

2. **Patch Extraction**  
   After registration, split the WSIs into patches and organize them into the following directory structure:


```text
dataset/
├── A/
│   └── train/
└── B/
    └── train/
```


   Here, `A` and `B` represent two different staining types (e.g., H&E and IHC).

3. **Dataset Preparation**  
Navigate to the `datasets/` directory and run the `combine_A_and_B` script to create the combined training dataset.

4. **Configure Training Options**  
Edit the parameters in `base_options.py` and `train_options.py` according to your experiment requirements.

5. **Start Training**  
Run the training script to start the model training process.

