# tensorflow-metal-sample

Try to use M1 Max GPU for deep learning in Tensorflow-Metal.

## Environment setup

```bash
curl -L -O https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh
chmod +x Miniforge3-MacOSX-arm64.sh 
sh Miniforge3-MacOSX-arm64.sh -b -p $(pwd)/miniforge3
source miniforge3/bin/actibate

conda create --name tensorflow_m1 python==3.9
conda activate tensorflow_m1

conda install -c apple tensorflow-deps
python -m pip install tensorflow-macos
python -m pip install tensorflow-metal
conda install -c conda-forge jupyter jupyterlab
```

## Run a sample script

```bash
$ time python train.py
313/313 - 1s - loss: 0.0746 - accuracy: 0.9785 - 1s/epoch - 3ms/step
python train.py  69.52s user 58.73s system 142% cpu 1:29.73 total
```