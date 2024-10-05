# CONSUL-IN-OKD
If you want to install consul in OKD you should create DIR in NFSSERVER or Your ShareFile server 
```
and give chmod 777 access to your file 
```
you need to deploy your yaml in okd and your config map 

and add this ENV to your Statefull ENVIRONMENT:
```
CONSUL_DISABLE_PERM_MGMT=yes
```
FOR CONNECT CONSUL TO YOUR SERVICE AND YOUR DEPLOYMENT , GATEWAY ,,,, YOUR SHOULD ADD THIS ENV :
```
SPRING_PROFILES_ACTIVE = dev,no-liquibase
SPRING_CLOUD_CONSUL_HOST = #YOUR CONSUL ADDRESS (WHEN YOU ROUTE IT) 
SPRING_CLOUD_CONSUL_PORT = # YOUR SV PORT 

```
FINISHE . 
:)
*YOUR PVC CREATE AUTOMATIC*
# You should have 2 pv  Becaues if Consul pods get down another is continue running 