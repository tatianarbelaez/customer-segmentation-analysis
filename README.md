# start
```sh
jupyter lab --ip='0.0.0.0' --no-browser
```

# Install conda
Download script from https://docs.conda.io/en/latest/miniconda.html#linux-installers, then:
```sh
sh Miniconda3-py39_4.11.0-Linux-x86_64.sh
```

# Create env and install dependencies
```sh
conda env create --name customer_segmentation -f environment_customer_segmentation.yml
```

# Activate env
```sh
conda activate customer_segmentation
jupyter notebook
```

# Delete env
```sh
conda activate base
conda env remove -n customer_segmentation
conda deactivate
```

# Install new deps
```sh
conda install seaborn=0.11.1
# then update yml
conda env export --from-history > environment_customer_segmentation.yml
```

# Update yml file
```sh
conda activate customer_segmentation
conda env export --from-history > environment_customer_segmentation.yml
```

# install debbuger
```sh
# -n = --name
# -c = --channel
# https://github.com/jupyterlab/debugger
# conda install -n customer_segmentation -c conda-forge jupyterlab=3 "ipykernel>=6" xeus-python
conda install -n customer_segmentation -c conda-forge nodejs xeus-python=0.8.6 ptvsd jupyterlab=2

conda install -n customer_segmentation ipykernel

jupyter labextension install @jupyterlab/debugger
jupyter lab build
XEUS_LOG=1 jupyter lab --no-browser --watch
```

# Optional?
```sh
conda install -c districtdatalabs yellowbrick
pip install *missings*
conda install -c conda-forge ipywidgets
jupyter nbextension enable --py widgetsnbextension
conda install ipywidgets==7.4.2

conda install -n base -c conda-forge widgetsnbextension
conda install -n customer_segmentation -c conda-forge ipywidgets

conda install xeus-python -c conda-forge
jupyter labextension install @jupyterlab/debugger
jupyter labextension install @jupyter-widgets/jupyterlab-manager
jupyter labextension install @jupyter-widgets/jupyterlab-manager jupyter-matplotlib
jupyter labextension install js
```

# delete in future

```sh
pip install pip install ipywidgets
pip install ipywidgets
pip install yellowbrick
pip install pixiedust
pip install pixiedust_node
conda install jupyterlab=3 "ipykernel>=6" xeus-python
pip install xeus-python
conda install xeus-python -c conda-forge
jupyter labextension install @jupyterlab/debugger
conda install "ipykernel>=6"
conda install -c conda-forge xeus-python
```
