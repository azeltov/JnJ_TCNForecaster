Dependencies are always tricky to get right, especially with machine learning, where there can often be a dizzying web of specific version requirements. You can re-create an Azure Machine Learning environment on your local machine either as a complete conda environment or as a Docker image by using the build_local() method of the Environment class:

```
ws = Workspace.from_config()
myenv = Environment.get(workspace=ws, name="tutorial-env", version="1")
myenv.build_local(workspace=ws, useDocker=False) #Creates conda environment.
```
If you set the build_local() useDocker argument to True, the function will create a Docker image rather than a conda environment. If you want more control, you can use the save_to_directory() method of Environment, which writes conda_dependencies.yml and azureml_environment.json definition files that you can fine-tune and use as the basis for extension.

The Environment class has a number of other methods for synchronizing environments across your compute hardware, your Azure workspace, and Docker images. For more information, see Environment class.

After you download the model and resolve its dependencies, there are no Azure-defined restrictions on how you perform scoring, fine-tune the model, use transfer learning, and so forth

https://docs.microsoft.com/en-us/azure/machine-learning/how-to-deploy-local#deploy-as-a-local-web-service-by-using-docker
