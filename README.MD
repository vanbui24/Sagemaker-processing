## Flowty Image

### Overview

This example will build a Docker Image from a local Dockerfile and push the image to AWS ECR. 
We need the ECR image address when creating the processing container with the required packages and other dependencies inside the container to process the script.

Clone the git repository by running the following in a local jupyter notebook (Python 3)
```
!git clone https://github.com/vanbui24/Sagemaker-processing.git
```

### Dockerfile
The first cell will write the docker file 

### Build and push the custom Docker Image to AWS ECR
The second cell will build and push the Docker Image to AWS ECR.

### Processing code
In the next cell, we write our processing code in a file, which SageMaker will upload to the processing container and use in the processing job.

### Using it with Sagemaker ScriptProcessor
In the first cell, we need to set the ecr_image, which we created in previous step. We also set the role_arn with permission to read and write to the s3 bucket. We choose the numbers of instances (instance_count) and choose the instance_type. 

In the Sagemaker-processing folder: Open the sagemaker-processing notebook

In the next cell we set the alias, and instance_name, and specify the output_bucket. When we run the cell, the processing job begins and SageMaker uploads the processing script to the container. Once the processing job is done SageMaker will save the output data (objective value, variable values and mygraph) as a CSV file to the assigned Amazon S3.


