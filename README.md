# pokemon-generator

Generating new pokemon image based on the kaggle dataset: https://www.kaggle.com/datasets/kvpratama/pokemon-images-dataset
Using DCGANs and VAEs

Update Anaconda Environment YML: `conda env export > pokemon-generator.yml`

# Using Anaconda Environment from VSCode

1.) Install the envirnoment from the YML
2.) Either activate the environment from Anaconda prompt or from cmd within VSCode (add new terminal of type cmd).
3.) Select the corresponding python interpreter on the top right of the notebooks.

# Current Breaking Change in Pytorch Lightning Loggers
Currently using the models from Lightning-Bolts has compatibility issues with Pytorch Lightnings Base Logger implementation.
Some name change of the BaseLogger causes import errors, which is currently being adressed: [Github Issue On Lightning Bolts](https://github.com/Lightning-AI/lightning-bolts/issues/962). To Fix the import error temporarily apply the [Suggested Fix](https://github.com/Lightning-AI/lightning-bolts/pull/965/files#diff-ffde2f26ed0c98921e4ec6551e20f8ba4a418bb468e6777af13df411ecedc514) in `*\miniconda3\envs\pokemon\Lib\site-packages\pl_bolts\callbacks\data_monitor.py`
to run the VAE.ipynb 