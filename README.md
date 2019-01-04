The version of FastAI used to run my skin lesion detection. Using V0.7 installation instructions below. Full installation instructions and debugging [here](https://forums.fast.ai/t/fastai-v0-install-issues-thread/24652).


## Installation

**If you're on windows** follow [this guide](http://forums.fast.ai/t/howto-installation-on-windows/10439), instead.

First, please make sure you have the latest `conda` and/or `pip`, depending on the package manager you use:

    pip install pip -U
    conda update conda

Currently, there are two ways to install fastai-0.7.x: (1) via conda from git source (best), or (2) via pip package (outdated code):

1. **Conda installation** from source:

   **1a.** First, create the `fastai` conda environment. It will install all the dependencies that are needed. Do it only once:
   ```
   git clone https://github.com/sean-mcmahon/fastai
   cd fastai
   conda env create -f environment.yml
   ```
   You then activate that environment with:
   ```
   conda activate fastai
   ```
   If you don't have GPU, build the `fastai-cpu` environment instead:
   ```
   git clone https://github.com/sean-mcmahon/fastai
   cd fastai
   conda env create -f environment-cpu.yml
   ```
   You then activate that environment with:
   ```
   conda activate fastai-cpu
   ```
   Windows users wanting to use their own GPU, rather than cloud or vm solutions, will have extra steps to take. Please see the links to windows-dedicated threads at the end of this post.

   **1b.** and now you can start running the course notebooks:
   ```
   jupyter notebook
   ```
   Once the jupyter notebook environment has started, in your browser navigate to `courses/dl1/lesson1.ipynb`  and execute the notebook.

   From now on remember that you need to activate either `fastai` or `fastai-cpu` environment that you created before in the shell that you code or notebooks from. 

    -----

   Some time later, to update to the latest `fastai-0.7.x.` code base:
   ```
   cd fastai
   git pull
   conda env update
   ```
   ---

   If something gets messed up, delete the old env first:
   ```
   conda env remove -y -n fastai
   ```
   or with `fastai-cpu`
   ```
   conda env remove -y -n fastai-cpu
   ```
   and then re-create the environment as explained in steps 1 a+b above.

   [This  post](http://forums.fast.ai/t/truncated-notebooks/24533/7) goes into more exact details on what else you might need to undo and restart from scratch. This probably mostly affects people who are updating their old setup, which no longer functions.

2. **Pip installation**

   ```
   pip install fastai==0.7.0
   pip install torchtext==0.2.3
   ```
   This currently will install the fastai version from May 13, 2018 (outdated)

If you have any issues with the installation see the FastAI wiki [here](https://forums.fast.ai/t/fastai-v0-install-issues-thread/24652).


## Copyright

Copyright 2017 onwards, fast.ai, Inc. Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. A copy of the License is provided in the LICENSE file in this repository.
