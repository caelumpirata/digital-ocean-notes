# digital-ocean-notes
repository includes - deployment - service - ingress.yaml files along with NOTES



Download Doctl for Windows
--------------------------
https://github.com/digitalocean/doctl/releases

Choose the package ends with  (doctl.1.xx.x-windows-amd64.zip)
 extract the zip and open the terminal in the same directory where doctl.exe is present 



Connect Doctl to the cluster
----------------------------
:-) download Config File !

Open terminal in the folder where doctl.exe is already present

Step 1: doctl auth init -t "TOKEN_FROM_CONFIG_FILE"

Step 2: Open Digital Ocean control panel
        go to KUBERNETES tab in MANAGE section
        click on cluster name
        
        in Overview section, go to CONNECTING TO KUBERNETES section
        -> copy automatically cluster certificate renewal command
        
        paste in terminal and run
        
Step 3: Verify your connectivity using following commands:
            kubectl cluster-info
            kubectl get nodes
        


Steps to follow
---------------------------------------

Step 1: Install Ngnix from 

        https://artifacthub.io/packages/helm/ingress-nginx/ingress-nginx
        
        useful commands:
            helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
            helm repo update
            helm install ingress-nginx ingress-nginx/ingress-nginx
            
            
Step 2: Deploy deployment.yaml,
               service.yaml and
               ingress.yaml file.
               
               
Step 3: Configure the domain in DIGITAL OCEAN networking panel 
          add one sub-domain in A tab.
          
          
          
 THINGS TO KEEP IN MIND (this is what i understood and yes, it worked)
 ----------------------------------------------------------------------
1.  containerPort == Port 
2.  targetPort == 8080

Videos for Reference
--------------------
1. Securing Kubernetes Ingress With Let’s Encrypt - 
        https://youtu.be/MpovOI5eK58
2. Practical Kubernetes Networking: How to Use Kubernetes Services to Expose Your App
        https://youtu.be/SoByggox15g
