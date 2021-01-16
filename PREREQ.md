For setting up cloudwatch agent >> https://www.eksworkshop.com/intermediate/250_cloudwatch_container_insights/cwcinstall/

For metrics server pre-req when setting up influxdb / heapster: https://docs.aws.amazon.com/eks/latest/userguide/metrics-server.html

K8s dashboard: https://github.com/kubernetes/dashboard/releases

URL: http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/login

token command: kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')

patching new storage class for stateful app volume persistence: kubectl patch storageclass appsc -p '{"metadata":{"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}' --namespace=stateful 

to undefault the original gp2 class created automatically with the cluster: kubectl patch storageclass gp2 -p '{"metadata":{"annotations":{"storageclass.kubernetes.io/is-default-class":"false"}}}' --namespace=stateful 

create a new secret for mysql db- kubectl create secret generic my-sql-pass --from-literal=password=<whatever your password is> --namspace=stateful 

EFS pre req for worker nodes - enable efs utils >> sudo yum install -y amazon-efs-utils 

mount target in efs >> put nodegroup SG with efs in default VPC 