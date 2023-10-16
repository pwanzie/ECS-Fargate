download the application
## Push image to ECR.
```
aws ecr get-login-password --region <region where ecr was create> | docker login --username AWS --password-stdin <your Repository URI>
```
Now let's go ahead and tag our image then push it to ECR
```
docker tag myimage <ECR URI>:dev
```
After tagging, you can now push the image to your ECR repository.
```
docker push <ECR URI>:dev
```
