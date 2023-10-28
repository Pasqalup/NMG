# NMG - A Neural Music Generator

## Usage

Start by cloning this repository:
```
git clone https://github.com/Pasqalup/NMG.git'
cd NMG
```
**Find all DELETE_ME files found in the [notebooks/](notebooks/) folder and delete them**

## 1. Installation
  Requires Anaconda or Miniconda<br />
  Using Linux reccommended

  - ### Create an environment
    ```
    conda create -n NMG python=3.9
    ```
  - ### Install Tensorflow
     - #### Linux GPU:
      ```
      conda install -c conda-forge cudatoolkit=11.8.0
      python3 -m pip install nvidia-cudnn-cu11==8.6.0.163 tensorflow==2.12.*
      mkdir -p $CONDA_PREFIX/etc/conda/activate.d
      echo 'CUDNN_PATH=$(dirname $(python -c "import nvidia.cudnn;print(nvidia.cudnn.__file__)"))' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
      echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/:$CUDNN_PATH/lib' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
      source $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
      # Verify install:
      python3 -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
      ```
      - #### WSL GPU [^1]:
      > See https://docs.nvidia.com/cuda/wsl-user-guide/index.html   
      Follow previous instructions for [Linux](#linux-gpu) installation
        
      - #### Windows Native GPU [^1][^2]:
      > See https://github.com/microsoft/tensorflow-directml-plugin#tensorflow-directml-plugin-    
        
    ### For CPU [^1]:
      ```
      pip install tensorflow-cpu==2.12.*
      ```
    ### Install other dependencies
    ```
    pip install -r requirements.txt
    ```
## 2. Usage    
  &emsp;&emsp;**Find all DELETE_ME files found in the [notebooks/](notebooks/) folder and delete them**    
  &emsp;&emsp;For now, run the three notebooks sequentially. This project is still in early development and may not generate promising results.

[^1]: Not yet tested
[^2]: This software is still under early development and you may run into issues. It is recommended that you use WSL Instead.
