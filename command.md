# Install EKS cluster on your machine



### Deploy-to-eks-using-github-actions

1. Create an EKS Cluster using this command:

# Create EKS cluster
  eksctl create cluster --name eks-cluster-110 --node-type t2.small --nodes 2 --nodes-min 2 --nodes-max 3 --region eu-west-2

# Get EKS Cluster service
eksctl get cluster --name eks-cluster-110 --region eu-west-2
 
 # Update eks kubeconfig once k8s cluster is installed successfully
aws eks update-kubeconfig --name eks-cluster-110

# Workflow for github actions

2. Then create .github folder and then create workflow folder inside .github folder 
3. create file with .yml extension and write the workflow code
4. Create a github repository 
5. Create secrets in github repo
        Go to settings of repo
        click on secrets and variables
6. Test application by getting the dns name and going to a web browser

Clean up: Run: eksctl delete cluster --name eks-cluster-110

## ==========================================================

## To test run the node.js application locally run the following command
npm init -y
 npm --version
 node -v
 npm install express --save
 

# to generate packet.json and packetlock.json and 
# to install exppress
npm install express