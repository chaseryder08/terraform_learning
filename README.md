# Terraform/IAC Udemy notes

## Manual set up VPC
## STEPS in order (TASKS) :
1) Create VPC
![img](images/main_vpc_outline.PNG)
2) Create Subnets 
![img](images/subnet.PNG)
- create multiple private and public subnets across 3 AZ
- 1 public/1 private subnet per AZ
1) Create IGW 
- attach IGW to VPC
![img](images/igw.PNG)
1) Create NAT gateway
![img](images/nat.PNG)
1) Create public and private route tables:
![img](images/rtb_associate.PNG)
- associate private and public subnets to our route tables
![img](images/rtb_public_igw.PNG)
- route public rtb to IGW - to go out to internet
![img](images/private_rtb_nat.PNG)
- route private rtb to NAT gateway, to access outside internet

---

# Clear point
- Terraform state file compares current infrastructure, and applys any changes to match
what is defined in that state file
