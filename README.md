Step 1: Create the environment
Run conda env create -f mlflow_exp.yml to create the conda environment from the YAML file.

Step 2: Activate the environment
Run conda activate <env_name> (replace <env_name> with the name given inside mlflow_exp.yml).

Step 3: Start MLflow server
Run mlflow server --port 5000 in the terminal and keep it running.

Step 4: Set tracking in your Python code
Inside your training script, add mlflow.set_tracking_uri("http://localhost:5000") before starting the MLflow run.

Step 5: Run your project
Run your training file using python train.py, then open http://localhost:5000 in your browser to see experiments, metrics, and results.
