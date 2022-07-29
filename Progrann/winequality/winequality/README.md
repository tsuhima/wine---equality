# winequality

1. Create a EMR in AWS with 1 master and 4 slave
2. Log in to master EC2
3. Run dependency.sh, it will install all the required dependency
4. All the required CSV files are uploaded in S3 under source-data folder
5. Run Training.py as "spark-submi Training.py" - This will train and save the model in S3 under data-output and prints the F1 score
6. Log in to the docker hub repo
7. In the master run docker to build a container - "sudo docker run --name pa2validate-container cs62/pa2validate-aws". This will take the repository from the Docker hub and create the container.
8. The container runs the validationData.csv and prints Test Error
Link to docker hub image: [docker hub](https://hub.docker.com/repository/docker/cs62/pa2validate-aws)
