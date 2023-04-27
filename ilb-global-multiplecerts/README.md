 # ILB with multiple certificates, fixed IP and global access

You can use the example manifests in this folder to configure a Gateway and an L7 Google Internal Load balancer, to expose a single service, accessible with 2 hostnames ([store.example.com](store.example.com), [store2.example.com](store2.example.com)) from a GKE cluster and terminating TLS with  2 certificates (one for each hostname) using Kubernetes secrets named `store-example-com` and `store2-example-com.`

The `global-access.yaml` manifests creates a policy to enable global access on your L7 ILB and make the service available also to other regions.

Before applying the manifests you must:

1. Create the 2 certificates and related Kubernetes secrets
2. Create a static IP in a subnet in the same VPC and region of your GKE cluster nodes and name it `gw-store-internal-address`
