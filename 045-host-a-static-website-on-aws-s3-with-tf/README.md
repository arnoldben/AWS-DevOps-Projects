# Host a Static Website on AWS (S3) with Terraform

## Overview
This project demonstrates how to configure a static website on Amazon S3 using Terraform. The setup involves utilizing Amazon S3 for hosting static content. The provided scripts and configuration files automate the process of setting up a static website on Amazon S3.

## Reference Diagram
![Reference Diagram](045-host-a-static-website-on-aws-s3-with-tf/images/archdiag_v1_2023-02_hoststaticwebsite_aws(s3)_tf.png)

## Project Components
- **Amazon S3**: Serves as the origin for storing and hosting static website files.

## Prerequisites
Before you begin, ensure you have the following:
- An AWS account with appropriate permissions to create S3 buckets and IAM policies.
- Terraform installed on your local machine.

## Notes
- Ensure that you have the necessary AWS credentials configured on your system for Terraform to authenticate with AWS.
- Review the Terraform configuration files to understand the resource provisioning process.
- Refer to the official Terraform documentation for more information on configuring AWS resources using Terraform.

## High-level Configuration Steps
(as described on https://docs.aws.amazon.com/AmazonS3/latest/userguide/HostingWebsiteOnS3Setup.html)

1. Create a Bucket
2. Enable Static Website Hosting
3. Edit Block Public Access Settings
4. Add a Bucket Policy
5. Configure an Index Document
6. Configure an Error Document
7. Test Your Website Endpoint
8. Cleanup

## Deployment Steps
1. **Clone Repository**: Clone the repository to your local machine.
2. **Configure Terraform**: Update the necessary variables in the Terraform configuration files.
3. **Initialize Terraform**: Run `terraform init` to initialize the working directory.
4. **Create Resources**: Run `terraform apply` to create the AWS resources.
5. **Configure Static Website**: Follow the steps outlined in the Terraform scripts to configure the static website on Amazon S3.
6. **Test Website**: Access the provided website URL to verify the functionality of the static website.
7. **Cleanup**: After testing, run `terraform destroy` to remove the resources created by Terraform.

## Resources
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)
- [Terraform Documentation](https://developer.hashicorp.com/terraform/docs)
