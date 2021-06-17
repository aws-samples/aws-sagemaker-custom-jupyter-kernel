# aws-sagemaker-custom-jupyter-kernel

## Introduction
There are several built-in Juptyer Kernels ready-to-use when working on an AWS Sagemaker Jupyter Notebook Instance.
They are easy to use but generally not convenient to customize:

- If you want to install new packages to the built-in Juptyer Kernels, there is no guarantee that the new packages are compatible with the existing ones.
- Even if you can install new packages to the built-in Juptyer Kernels, you will lose the modified/custom kernels when restarting the Notebook Instance.

This repo provides a couple of easy-to-use template scripts to help you set up a custom jupyter kernel on a AWS Sagemaker Jupyter Notebook Instance. 


## Build/Start Custom Jupyter Kernel

### When first create the Jupyter notebook instance.
1. Need to edit `environment.yml` to specify your custom environment if you want to build a different Python Kernel to this example in this repo.
2. Run the command below to build the custom Python Kernel named `Conda_my-custom-jupyter-kernel`.
        
    ./build_env.sh
    
### (Optional): Every time re-start the Jupyter Notebook instance, run the command below to add the custom Python Kernel.

    ./start_env.sh

### To use the custom Kernel, create a new Jupyter notebook, and select `Conda_my-custom-jupyter-kernel` as the Python Kernel.

