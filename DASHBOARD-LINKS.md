For setting up cloudwatch agent >> https://www.eksworkshop.com/intermediate/250_cloudwatch_container_insights/cwcinstall/

For metrics server pre-req when setting up influxdb / heapster: https://docs.aws.amazon.com/eks/latest/userguide/metrics-server.html

K8s dashboard: https://github.com/kubernetes/dashboard/releases

URL: http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/login

token command: kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep eks-admin | awk '{print $1}')

