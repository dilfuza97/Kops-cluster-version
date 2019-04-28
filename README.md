# qa-dilfuza-cluster
1. export  KOPS_STATE_STORE


2. kops edit cluster


3. kubernetesVersion: 1.11.8  (change version) 



4. kops update cluster  (plan) 



5. kops update cluster --yes   (apply)



6. Scale out  ASG   from 3-6  



7. kubectl  get nodes --insecure-skip-tls-verify=true



8. kubectl  cordon ip-172-20-38-52.eu-west-1.compute.internal  --insecure-skip-tls-verify=true
     Put instance to maintenance mode 
     
     
     
     

9. kubectl  drain ip-172-20-38-52.eu-west-1.compute.internal   --ignore-daemonsets  --insecure-skip-tls-verify=true
     Remove pods running in this node. 
     
     
     

10. kubectl  get pods --all-namespaces  --insecure-skip-tls-verify=true
    Verify pods scheduled properly. 
