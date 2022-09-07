# digital-ocean-notes
repository includes - deployment - service - ingress.yaml files along with NOTES


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
1.  containerPort == targetPort 
2.  port == 80

Videos for Reference
--------------------
1. Securing Kubernetes Ingress With Let’s Encrypt - 
        https://youtu.be/MpovOI5eK58
2. Practical Kubernetes Networking: How to Use Kubernetes Services to Expose Your App
        https://youtu.be/SoByggox15g
