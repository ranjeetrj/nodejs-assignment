# nodejs-assignment
Assignment given by Company

-----------There should be 10 replicas running-----------

   maxReplicas: 10
  
  ---------The deployment should autoscale at average 50% cpu and 60% memory.-----------
  
    metrics:
    - resource:
        name: cpu
        targetAverageUtilization: 50
        name: memory
        targetAverageUtilization: 60
      type: Resource
      
 -------------------Use a custom docker image hosted on ECR called nodejs-test:latest (any region).
 ------------------ Bonus points if you include how to login and pull an image from ECR.	------
 
aws configure set aws_access_key_id ACCESS_KEY
aws configure set aws_secret_access_key SECRET_KEY
aws configure set default.region YOUR_DEFAULT_REGION
aws configure set default.output json
aws ecr get-login-password --region REGION | docker login --username USER --password-stdin <REPO_NAME>
docker pull <REPO>/<IMAGE_NAME>
  
 ------------Any change to the deployment should always ensure at least 7 replicas are running at all times.--------------
 
    minReplicas: 7

------ Bonus points if you do the task as code i.e. using terraform or any other configuration language of your choice----

Currently I am learning the terraform.
  
  
  
