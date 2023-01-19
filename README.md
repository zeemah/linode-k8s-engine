# linode-k8s-engine
## Installing a Stateful App On K8s using helm


#### Overview of what I built/deployed

    1. Deploy mongodb in Linode cluster using helm
    2. create 3 replicas using statefulset
    3. configure data persistence with linode's cloud storage
    4. deploy UI client (mongo-express)
    5. configure nginx-ingress

#### NOTE:Before the above, 
    
    1. create 2 k8s node on linode and download the test-kubeconfig.yaml file
    2. cd into the folder you saved it in 
    3. to connect to the nodes locally, set kubconfig.yaml as an environmental variable using your cli 
        for linux systems:
        "export KUBECONFIG=test-kubeconfig.yaml"

        on powershell:
        " $env:KUBECONFIG='test-kubeconfig.yaml' "

    4. run the following command to see your nodes locally on your terminal
        "kubectl get node"


    5. Add mongodb helm chart
        "helm repo add bitnami https://charts.bitnami.com/bitnami"