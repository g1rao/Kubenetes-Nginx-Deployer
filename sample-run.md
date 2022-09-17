jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --help
usage: knd [-h] [-f] [-l] [-n <nginx-version>] [-r <no-of-replicas>] [-v] [deployment-name]

Kubernetes Nginx Deployer

positional arguments:
  deployment-name                                      Specify deployment name

optional arguments:
  -h, --help                                           show this help message and exit
  -f, --force                                          Removes existing deployment with specified name and recreates
  -l, --list-deployments                               List the deployements
  -n <nginx-version>, --nginx-version <nginx-version>  Specify nginx version
  -r <no-of-replicas>, --replicas <no-of-replicas>     Specify no of replicas
  -v, --verbose                                        Print debug messages
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --list-deployments
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  1
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4 --force nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  1
[17/09/2022 10:20:06 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:20:06 PM] INFO: Updating container image to nginx:1.15.4
[17/09/2022 10:20:06 PM] INFO: Deployment is being updated to nginx:1.15.4
100%|████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:00<00:00, 894307.89it/s]
[17/09/2022 10:20:06 PM] INFO: Deployment image is updated to nginx:1.15.4
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  1
[17/09/2022 10:20:06 PM] INFO: Deployment nginx-deployment is being deleted.
[17/09/2022 10:20:14 PM] INFO: Deployment nginx-deployment has been deleted.
DeploymentName                Image                         Replicas
[17/09/2022 10:20:14 PM] INFO: Deployment nginx-deployment is being created...
100%|████████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:05<00:00, 19.74it/s]
[17/09/2022 10:20:19 PM] INFO: Deployment nginx-deployment has been created and ready to use...
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  1
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --list-deployments
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  1
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4 --force --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  1
[17/09/2022 10:20:40 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:20:40 PM] INFO: Deployment is being scaled to 4
100%|████████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:05<00:00, 19.75it/s]
[17/09/2022 10:20:45 PM] INFO: Deployment is scaled to 4
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
[17/09/2022 10:20:45 PM] INFO: Deployment nginx-deployment is being deleted.
[17/09/2022 10:20:47 PM] INFO: Deployment nginx-deployment has been deleted.
DeploymentName                Image                         Replicas
[17/09/2022 10:20:47 PM] INFO: Deployment nginx-deployment is being created...
100%|████████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:05<00:00, 19.72it/s]
[17/09/2022 10:20:52 PM] INFO: Deployment nginx-deployment has been created and ready to use...
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4  --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
[17/09/2022 10:21:02 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:21:02 PM] INFO: No changes made to cluster...
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version latest  --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
[17/09/2022 10:21:10 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:21:10 PM] INFO: Updating container image to nginx:latest
[17/09/2022 10:21:10 PM] INFO: Deployment is being updated to nginx:latest
100%|███████████████████████████████████████████████████████████████████████████████████| 100/100 [00:00<00:00, 1997287.62it/s]
[17/09/2022 10:21:10 PM] INFO: Deployment image is updated to nginx:latest
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4  --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  4
[17/09/2022 10:21:15 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:21:15 PM] INFO: Updating container image to nginx:1.15.4
[17/09/2022 10:21:15 PM] INFO: Deployment is being updated to nginx:1.15.4
100%|███████████████████████████████████████████████████████████████████████████████████| 100/100 [00:00<00:00, 1353001.29it/s]
[17/09/2022 10:21:15 PM] INFO: Deployment image is updated to nginx:1.15.4
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --list-deployments
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  3
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version latest  --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
[17/09/2022 10:21:51 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:21:51 PM] INFO: Updating container image to nginx:latest
[17/09/2022 10:21:51 PM] INFO: Deployment is being updated to nginx:latest
100%|███████████████████████████████████████████████████████████████████████████████████| 100/100 [00:00<00:00, 1331525.08it/s]
[17/09/2022 10:21:51 PM] INFO: Deployment image is updated to nginx:latest
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4  --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  4
[17/09/2022 10:22:07 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:22:07 PM] INFO: Updating container image to nginx:1.15.4
[17/09/2022 10:22:07 PM] INFO: Deployment is being updated to nginx:1.15.4
100%|███████████████████████████████████████████████████████████████████████████████████| 100/100 [00:00<00:00, 1393456.48it/s]
[17/09/2022 10:22:07 PM] INFO: Deployment image is updated to nginx:1.15.4
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4  --replicas 3 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
[17/09/2022 10:22:15 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:22:15 PM] INFO: Deployment is being scaled to 3
100%|████████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:05<00:00, 19.75it/s]
[17/09/2022 10:22:20 PM] INFO: Deployment is scaled to 3
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  3
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version 1.15.4  --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  3
[17/09/2022 10:23:57 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:23:57 PM] INFO: Deployment is being scaled to 4
100%|████████████████████████████████████████████████████████████████████████████████████████| 100/100 [00:05<00:00, 19.71it/s]
[17/09/2022 10:24:02 PM] INFO: Deployment is scaled to 4
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version latest --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:1.15.4                  4
[17/09/2022 10:24:11 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:24:11 PM] INFO: Updating container image to nginx:latest
[17/09/2022 10:24:11 PM] INFO: Deployment is being updated to nginx:latest
100%|███████████████████████████████████████████████████████████████████████████████████| 100/100 [00:00<00:00, 1191563.64it/s]
[17/09/2022 10:24:11 PM] INFO: Deployment image is updated to nginx:latest
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  4
jtalagan@jtalagan-mac Kubenetes-Nginx-Deployer % knd --nginx-version latest --replicas 4 nginx-deployment
DeploymentName                Image                         Replicas
nginx-deployment              nginx:latest                  4
[17/09/2022 10:24:23 PM] INFO: nginx-deployment is already exists.
[17/09/2022 10:24:23 PM] INFO: No changes made to cluster...