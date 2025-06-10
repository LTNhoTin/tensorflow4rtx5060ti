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
# Create a new directory for testing TensorFlow installation
mkdir -p ~/tensorflow_test

# Create a virtual environment with Python 3.10 (crucial to use the same Python version)
python3.10 -m venv ~/tensorflow_test/venv

# Activate the virtual environment
source ~/tensorflow_test/venv/bin/activate

# Verify Python version in the virtual environment
python --version
# Should output: Python 3.10.x

# Install the TensorFlow wheel file
pip install https://github.com/weyn9q/rtx5070tensorflow/releases/download/v1.0/tensorflow-2.20.0.dev0+selfbuilt-cp310-cp310-linux_x86_64.whl

# Test TensorFlow installation and GPU detection
python -c "import tensorflow as tf; print(f'TensorFlow version: {tf.__version__}'); print(f'GPU available: {tf.config.list_physical_devices(\"GPU\")}'); print('GPU test:', tf.test.is_gpu_available())"
