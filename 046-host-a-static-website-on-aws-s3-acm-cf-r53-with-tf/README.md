# Host a Static Website on AWS (S3, ACM, CF, R53) with Terraform

## Overview

This project demonstrates how to deploy a static website on Amazon Web Services (AWS) using Terraform. The setup includes configuring SSL encryption with AWS Certificate Manager (ACM), utilizing Amazon S3 for hosting static content, deploying a content delivery network (CDN) with CloudFront, and managing DNS routing with Route 53.

## Reference Diagram

![Reference Diagram](/images/archdiag_v1_2023-02_hoststaticwebsite_aws(s3,acm,cf,r53)_tf.png)

## Project Components

- **Amazon S3**: Serves as the origin for storing and hosting static website files.
- **AWS Certificate Manager (ACM)**: Provides SSL/TLS certificates for securing the website.
- **CloudFront (CF)**: Acts as a CDN to accelerate content delivery globally with low latency.
- **Route 53 (R53)**: Manages DNS routing to direct traffic to the CloudFront distribution.

## Prerequisites
Before you begin, ensure you have the following:
- An AWS account with appropriate permissions to create S3 buckets and IAM policies.
- Terraform installed on your local machine.

## Notes
- Ensure that you have the necessary AWS credentials configured on your system for Terraform to authenticate with AWS.
- Review the Terraform configuration files to understand the resource provisioning process.
- Refer to the official Terraform documentation for more information on configuring AWS resources using Terraform.

## Deployment Steps
1. **Clone Repository**: Clone the repository to your local machine.
2. **Configure Terraform**: Update the necessary variables in the Terraform configuration files.
3. **Initialize Terraform**: Run `terraform init` to initialize the working directory.
4. **Create Resources**: Run `terraform apply` to create the AWS resources.
5. **Test Website**: Access the provided website URL to verify the functionality of the static website.
6. **Cleanup**: After testing, run `terraform destroy` to remove the resources created by Terraform.
   
## How CloudFront Delivers Content

1. **Client Request**: The client requests a file from the website.
2. **DNS Routing**: Route 53 routes the request to the nearest CloudFront edge location.
3. **Edge Location Search**: CloudFront searches for the requested file in its cache at the edge location.
4. **File Retrieval**: If the file is found, CloudFront immediately serves it to the client. Otherwise, it forwards the request to the origin (S3 bucket).
5. **Origin Retrieval**: The origin retrieves the requested file and sends it back to the CloudFront edge location.
6. **Content Delivery**: CloudFront delivers the file to the client and adds it to its cache for future requests.

## Resources
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)
- [Terraform Documentation](https://developer.hashicorp.com/terraform/docs)

## Additional Notes

- Customize Terraform scripts and configurations as needed for your specific requirements.
- Ensure proper IAM permissions and security measures are in place for managing AWS resources securely.
