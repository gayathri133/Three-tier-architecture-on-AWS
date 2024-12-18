# Three-tier-architecture-on-AWS

This project showcases the implementation of a **three-tier architecture** on AWS, designed for scalability, high availability, and enhanced security.  

## Architecture Overview  
The architecture is divided into three layers:  
1. **Presentation Layer**:  
   - Hosted on Amazon EC2 instances within a public subnet.  
   - Handles user interaction through a web interface.  

2. **Application Layer**:  
   - Hosted in a private subnet to process business logic securely.  
   - Ensures no direct user access for added security.  

3. **Database Layer**:  
   - Utilizes Amazon RDS for structured data storage.  
   - Placed in a private subnet for controlled access.  

### Key Features:  
- **Elastic Load Balancer (ELB)**: Ensures traffic is distributed evenly for high availability.  
- **Auto Scaling**: Dynamically adjusts resources to meet demand.  
- **Amazon S3**: Stores static content such as images or logs.  
- **Amazon VPC**: Provides network isolation and enhanced security.  
- **IAM Roles and Policies**: Ensure secure and limited access to AWS resources.  

## Setup Instructions  
Follow these steps to deploy the architecture:  

1. **Networking Setup**:  
   - Create a VPC with public and private subnets.  
   - Configure route tables and security groups to enable proper communication between layers.  

2. **Presentation Layer**:  
   - Launch EC2 instances in the public subnet.  
   - Configure an Elastic Load Balancer to manage incoming traffic.  

3. **Application Layer**:  
   - Set up EC2 instances in the private subnet.  
   - Deploy your application to handle business logic.  

4. **Database Layer**:  
   - Create an Amazon RDS instance in the private subnet.  
   - Configure the database to accept requests only from the application layer.  

5. **Additional Configuration**:  
   - Enable Auto Scaling to handle traffic fluctuations.  
   - Configure IAM roles to grant specific permissions to resources.  

## Project Documentation  
For detailed architecture diagrams, configurations, and additional notes, refer to the [Project Document](link-to-document).  

## Future Enhancements  
- Implement AWS CloudFormation for automated deployment.  
- Use AWS CloudWatch for enhanced monitoring and logging.  
- Integrate CI/CD pipelines with AWS CodePipeline.  



