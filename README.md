This repository contains a cluster file + various services, deployments, statefulsets, storage components and a dashboard via Elastic Kubernetes Service.

Dashboard folder >> influxdb + heapster files to set up our kubernetes dashboard (for visualization + monitoring / logging purposes)

Elastic File Sharing folder >> EFS integration files for our kubernetes cluster to be able to use EFS volumes. 

Statefulset-wp-mysql folder >> service + statefulset files to deploy a wordpress application in our cluster.

Statelessapplication folder >> redis php guestbook application files, no persistent volumes in this one due to it being a statless app.

Stateful application folder >> another wordpress app but with persisted EBS volumes.

PREREQ file >> notes / little commands for documentation purposes and some pre requisites notes for setting up the dashboard.

rbac / aws-auth files >> user authentication for eks cluster. 

eksjawnt >> main cluster file. 

