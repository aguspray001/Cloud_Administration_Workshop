# Working with MySQL Database Service (MDS)
**To create MySQL DB System on MDS, please watch this Youtube video**: https://www.youtube.com/watch?v=dasutiDLTkM
</br>
</br>
**Skip step 1, 2, 3, because you've done it. Go directly to step 4**
</br>
</br>
1.	On the Navigation Menu, under Database, select MySQL -> DB Systems. 
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.39.07%20PM.png)
</br>
2.	On DB Systems in <Compartment Name> Compartment, click on Create MySQL DB System. 

![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.39.46%20PM.png)
</br>
3.	On Create MySQL DB System, under DB System Information, select a Compartment, enter a Name for the DB System, add a Description, select an Availability Domain, select a Fault Domain, select a configuration for the MySQL Shape, and click Next. 
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.40.32%20PM.png)
</br>
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.41.30%20PM.png)
</br>
4.	On Create MySQL DB System, under Database Information, create the Administrator Credentials by entering Username and Password, specify the network information selecting the Virtual Cloud Network and Subnet in the compartment and entering Hosting Name, and click Next.
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.48.33%20PM.png)
</br>
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.49.07%20PM.png)
</br>
5.	On Backup Information, select Enable Automatic Backups, select the Backup Retention Period, select Default Backup Window, and click on Create.
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.49.19%20PM.png)
</br>
6.	The New MySQL DB System will be ready to use after a few minutes. The state will be shown as Creating during the creation.  
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.49.44%20PM.png)
</br>
7.	The state Active indicates that the DB System is ready to use. Check the MySQL endpoint (Address) under Instances in the MySQL DB System Details page.
![Image of picture1](https://github.com/tripplea-sg/Cloud_Administration_Workshop/blob/main/Lab-7/Screenshot%202020-11-13%20at%202.50.18%20PM.png)
</br>
</br>
</br>
## Open Connection
1. Go to OCI Dashboard and Click Networking >> Virtual Cloud Network
2. Click your VCN below (sample: workshop-vcn)
3. Click Private Subnet 
4. Click the Security List
5. Add Ingress Rule (source: 0.0.0.0/24, TCP, All ... Destination: port 3306)
## Connect to your MDS from VM
```
mysqlsh {your_user}@{MDS_Internal_IP}:3306
```
Exit from Shell
```
\q
```



  
