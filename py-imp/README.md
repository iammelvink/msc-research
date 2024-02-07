# msc-research-project-implementation

## Repository for my msc-research-project-implementation project

## This is the Python section

Written in **Python**

1. Methodologies/Project Management:

   - Agile

2. Coding Practices:

   - OOP (Object Oriented Programming)
   - MVC (Model View Controller)

3. Programming Languages/Frameworks:

   - R
   - Python
   - PlantUML - Unified Modeling Language (UML)

## Live Demo (loading...)

- [dev](https://<>.amazonaws.com/dev 'dev')

## Instructions

1. Make sure you have these installed

   - [Mambaforge (faster Anaconda)](https://github.com/conda-forge/miniforge/releases/ 'Mambaforge (faster Anaconda)')
     - I used version 23.3.1-1 at time of creation

2. Clone `ONLY THE LATEST COMMIT` of this repository into your local machine using the terminal (mac) or
   [Gitbash (PC)](https://git-scm.com/download/win 'Gitbash (PC)') to save storage space

   ```sh
   git clone https://github.com/iammelvink/msc-research-project-2023.git --depth=1
   ```

3. ```sh
   cd "py-imp"
   ```

4. Setup Mambaforge base env

   ```sh
   mamba env update --name base --file tools-for-base.yml && mamba activate base
   ```

5. Setup mamba project env:

   ```sh
   mamba env create --name project_n --file tools-tf.yml && mamba activate project_n
   ```

   5.1. ONLY For Linux:

      ```sh
      sudo apt update && sudo apt upgrade -y
      ```

      ```sh
      sudo apt install nvidia-driver -< latest version available for your pc>
      ```

      ```sh
      sudo reboot
      ```

      ```sh
      nvidia-smi
      ```

      ```sh
      sudo prime-select query && sudo prime-select nvidia && sudo prime-select query
      ```

      ```sh
      mamba install -c conda-forge cudatoolkit=11.2 --yes && python -m pip install --force-reinstall --upgrade nvidia_cudnn_cu11==8.9.2.26
      ```

      ```sh
      python -m pip install --force-reinstall --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-2.10.1-cp38-cp38-manylinux_2_17_x86_64.manylinux2014_x86_64.whl && mamba install -c nvidia cuda-nvcc=11.3.58 --yes
      ```

      ```sh
      mkdir -p $CONDA_PREFIX/etc/conda/activate.d && echo 'CUDNN_PATH=$(dirname $(python -c "import nvidia.cudnn;print(nvidia.cudnn.__file__)"))' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh && echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/:$CUDNN_PATH/lib' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh && mkdir -p $CONDA_PREFIX/etc/conda/activate.d && printf 'export XLA_FLAGS=--xla_gpu_cuda_data_dir=$CONDA_PREFIX/lib/\n' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh && source $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh && mkdir -p $CONDA_PREFIX/lib/nvvm/libdevice && cp $CONDA_PREFIX/lib/libdevice.10.bc $CONDA_PREFIX/lib/nvvm/libdevice/
      ```

6. Setup "pip" project env:

   ```sh
   poetry install --all-extras
   ```

7. Add env to kernel:

   ```sh
   python -m ipykernel install --user --name project_n --display-name "Python 3.8 (project_n)"
   ```

8. Run JupyterLab

   ```sh
   jupyterlab
   ```

9. Open a `.ipynb` file in the `code` directory to get started

10. Enjoy!

## More Stuff

Check out some other stuff on
[Melvin K](https://github.com/iammelvink 'Melvin K GitHub page')
