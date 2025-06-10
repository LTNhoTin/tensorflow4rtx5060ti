# tensorflow4rtx5060ti# TensorFlow for RTX 5060TI (Custom Build)

This repository contains a custom-built TensorFlow wheel file optimized for NVIDIA RTX 5070TI GPUs.

## System Requirements

- **Python**: 3.10.x
- **CUDA**: 12.8.1
- **cuDNN**: 9.8.0
- **GPU**: NVIDIA RTX 5060 TI 
- **OS**: Ubuntu 24.04 

## Installation Instructions

```bash
# 1. Create a new Conda environment with Python 3.10
conda create -n ltnt python=3.10 -y
conda activate ltnt

# 2. Install the CUDA Toolkit 12.8.1
conda install nvidia/label/cuda-12.8.1::cuda-toolkit

# 3. Verify Python version
python --version
# Expected: Python 3.10.x

# 4. Install the custom TensorFlow wheel (self-built for RTX 5060 TI)
pip install https://github.com/weyn9q/rtx5070tensorflow/releases/download/v1.0/tensorflow-2.20.0.dev0+selfbuilt-cp310-cp310-linux_x86_64.whl

# 5. Test TensorFlow and GPU availability
python -c "import tensorflow as tf; print(f'TensorFlow version: {tf.__version__}'); print(f'GPU available: {tf.config.list_physical_devices(\"GPU\")}')"
