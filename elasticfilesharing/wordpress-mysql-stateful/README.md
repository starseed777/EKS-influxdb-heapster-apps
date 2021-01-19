Links used: https://github.com/kubernetes-retired/external-storage/tree/master/aws/efs/deploy

- I added an extra permission to persistent volumes - "create" + I had to add an EFS access policy to the nodegroup IAM role in order to sucessfully be able to secure permissions to create the efs volumes 

- In the code it was very simple same process to creating any other statefulset just had a big issue with the permissions while making this so the rbac and IAM role was what solved my personal bugs

- In essence we just had to give efs provisioner enough permissions for everything to work, by following the repo pasted above I was able to sucessfully authenticate efs-provisioner 
