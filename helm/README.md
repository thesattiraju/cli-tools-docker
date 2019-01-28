# helm docker

These images are based on alpine. 
Usage: `docker run clitools/helm`
Example: `docker run clitools/helm init`

Prereq: You need to mount your kubeconfig to the container for fetching information from cluster.

Say your kubeconfig is in a directory /home/user/.kube, mount this directory to the container by adding this to your run command `-m /home/user/.kube:/tmp` and set the KUBECONFIG environment variable on the flow.

Your command execution would look like `docker run clitools/helm -m /home/user/.kube:/tmp -env KUBECONFIG=/tmp/config <your kubectl commands>`