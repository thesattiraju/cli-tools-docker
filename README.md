# CLI Tools Docker based

Docker images for various tools. These images are based on alpine and pushed to docker hub registry under `clitools`.

Usage: `docker run clitools/<tool-name>`

Example: `docker run clitools/kubectl get svc`

### Prereq for kubernetes tools

You need to mount your kubeconfig to the container for fetching information from cluster.

Say your kubeconfig is in a directory /home/user/.kube, mount this directory to the container by adding this to your run command `-m /home/user/.kube:/tmp` and set the KUBECONFIG environment variable on the flow.

You need to add `-m /home/user/.kube:/tmp -env KUBECONFIG=/tmp/config` to your docker run commands
