# Day 5 - Look into the architecture of a Kubernetes cluster
No code again

Kuebernetes cluster are made up of master nodes (the control plane) and worker nodes.
It wasn't explained how multiple master nodes would interract/sync yet.

Master nodes handle all API requests from the kubectl client to adjust the cluster.
Worker nodes host pods.

Master nodes contain the API intrerface which interracts with:
    - The scheduler to find nodes into which pods will be hoster
    - A controller manager (which is in charge of the node controller, namespaces and deployment (This likely wasn't explained well))
    - etcd (a key value store), this is where all the secrets and cluster info is stored.

Worker nodes are comprised of:
    - kubelet, the main process that subscribes to a specific kubernetes cluster
    - kube-proxy, handles the between node and intra-node networking.
    - pods itself (individual units of grouped containers for scaling)
