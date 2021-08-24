# Local Setup

Build and activate the environment:

```
conda env create --file environment.yml \
&& conda activate pangeo-forge-example
```

Install the `pangeo-forge-example` conda enviroment as a Jupyter kernel:
```
python -m ipykernel install --user --name pangeo-forge-example
```

Launch JupyterLab:
```
jupyter lab
```

From JupyterLab, run the notebook `execute_recipe.ipynb` using the `pangeo-forge-example` kernel.

# IPFS integration

Note that in cell 4 of `execute_recipe.ipynb`, Pangeo Forge storage targets are instantiated using `fsspec.implementations.local.LocalFilesystem`.

If an `fsspec.implementations.ipfs.IPFSFilesystem` were to exist, this is where we would point to it.