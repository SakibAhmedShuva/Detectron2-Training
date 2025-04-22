# Detectron2 Training 🔥

A comprehensive implementation and training pipeline using Facebook's Detectron2 framework, showcasing instance segmentation with Mask R-CNN X101-FPN architecture.

## 🔑 Key Features

- Complete instance segmentation training pipeline
- Mask R-CNN X101-FPN backbone implementation
- Custom MAP-IOU evaluation metrics
- Advanced data preprocessing
- COCO format dataset compatibility
- Optimized training configurations
- Progress tracking with TensorBoard

## 🛠️ Technologies Used

- PyTorch
- Detectron2
- Albumentations
- COCO API
- NumPy
- Pandas
- OpenCV

## 📊 Model Architecture

- Base Model: Mask R-CNN
- Backbone: ResNeXt101-32x8d-FPN
- Training Strategy: 3x schedule
- ROI Heads Batch Size: 1024

## 💻 Installation

```bash
# Clone the repository
git clone https://github.com/SakibAhmedShuva/Detectron2-Training.git

# Install dependencies
pip install torch torchvision
pip install 'git+https://github.com/facebookresearch/detectron2.git'
pip install -r requirements.txt
```

## 📝 Training Configuration

The training pipeline is configured with the following specifications:

- Learning Rate: 0.0005
- Batch Size: 2
- Maximum Iterations: 20,000
- Learning Rate Steps: [7000, 9000]
- Warmup Iterations: 2000
- Evaluation Period: 500
- Checkpoint Period: 500

## 🚀 Usage

1. Prepare your dataset in COCO format
2. Update the paths in the notebook:
   ```python
   ANNOTATIONS_FILE_PATH = "path/to/your/annotations.json"
   IMAGES_DIR_PATH = "path/to/your/images"
   ```
3. Run the training notebook:
   ```bash
   jupyter notebook detectron2-training.ipynb
   ```

## 📈 Custom Evaluation Metric

The implementation includes a custom MAP-IOU evaluator:
- Threshold range: 0.5 to 0.95 (step: 0.05)
- Evaluation period: Every 500 iterations
- Metrics tracked: True Positives, False Positives, False Negatives

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
