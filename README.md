# cloud-month
This CloudFormation template is used in tandem with this series of DevCentral articles.

This CFT creates the following resources:
<ul>
<li>A VPC with three subnets, each one in a different zone</li>
<li>An Amazon Elastic Load Balancer</li>
<li>Three Windows servers with IIS</li>
<li>One Windows server with a SQL database</li>
</ul>

When you're done deploying, you should be able to connect to the AWS ELB and view the website.

### Template Parameters ###
This CFT has the following parameters.  

| Parameter | Required | Description |
| --- | --- | --- |
| Stack Name | x | Name the template uses to create BIG-IP and AWS object names. |
| WindowsName1 | x | Name for the first Windows instance. |
| WindowsName2 | x | Name for the second Windows instance. |
| WindowsName3 | x | Name for the third Windows instance. |
| DBName | x | Name for the Windows instance that contains a SQL database. |
| KeyName | x | EC2 KeyPair to enable SSH access to the BIG-IP instance. |
| adminUsername | x | Username for accessing the Windows servers. The username can contain only alphanumeric characters, periods ( . ), underscores ( _ ), or hyphens ( - ). Note also that the user name cannot be any of the following: adm, apache, bin, daemon, guest, lp, mail, manager, mysql, named, nobody, ntp, operator, partition, password, pcap, postfix, radvd, root, rpc, rpm, sshd, syscheck, tomcat, uucp, or vcsa. |
| adminPassword | x | Password for accessing the Windows servers. |
| WindowsInstanceType | x | EC2 instance type. |
| WindowsAMI | x | An identifier for the Amazon Machine Image (AMI) that is used to create instances. To find the AMI ID, go to the AWS marketplace, find the product you want, click the Manual Launch tab, and note the AMI ID for the region where you’re going to deploy. |
| DBAMI | x | An identifier for the Amazon Machine Image (AMI) that is used to create the database instance. To find the AMI ID, go to the AWS marketplace, find the product you want, click the Manual Launch tab, and note the AMI ID for the region where you’re going to deploy. |
<br>
