
---

## 📌 Files Explained

### 🧾 Notebooks (`notebooks/`)

- **`Auto_segment.ipynb`**  
  Runs an **automatic segmentation pipeline** using SAM 2.1.  
  - No manual bounding box input required.  
  - Useful for batch processing of images.  
  - Demonstrates how SAM generalises segmentation.

- **`Segment_withBB.ipynb`**  
  Segments images **based on bounding box (BB) input**.  
  - Bounding boxes provide guidance to SAM for more controlled segmentation.  
  - Useful for cases where you want to focus on a specific region of interest.  

- **`train.ipynb`**  
  Notebook to **fine-tune SAM 2.1** on a custom dataset.  
  - Reads configuration from `train.yaml`.  
  - Handles dataset loading, training loop, and evaluation.  
  - Produces fine-tuned weights that can be reused in segmentation tasks.

---

### ⚙️ Config (`config/`)

- **`train.yaml`**  
  Configuration file containing paths and hyperparameters for training.  
  Example fields include:
  ```yaml
  dataset_path: "./data/"
  epochs: 50
  batch_size: 16
  learning_rate: 0.0005
  model_checkpoint: "./checkpoints/sam_finetuned.pth"

Weight for FineTuned Model : https://drive.google.com/drive/folders/1hT9alHnIrqR67jU3-j26zsUofmWaqBPu?usp=drive_link
