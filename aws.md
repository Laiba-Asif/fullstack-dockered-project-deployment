steps

1. create vpc with 2 public subnets and 2 private also configure zonal nat gateway  -> it will create subnets and route tables with nat gatewy and internet gateway as well.

2. before creating RDS first create Subnet groups 

2. create database RDS with my sql and choose your vpc , create new vpc security group with name ecs-rds-sg then create database
4. go to security groups and edit inbound rules delete prev rules and add new rule with type mysql/aurora and in source allow only backend security group to talk with database 
3. create parameter go to parameter store 

4. Create ECR with no scanning for frontend and backend

db pass = 7RXpfRcPuJV0U6dPdjKk
db endpoint = ecs-database-1.c7gegeg6i714.ap-south-1.rds.amazonaws.com