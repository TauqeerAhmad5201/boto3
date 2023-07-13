# boto3

The AWS SDK for Python (Boto3) provides a Python API for AWS infrastructure services. Using the SDK for Python, you can build applications on top of Amazon S3, Amazon EC2, Amazon DynamoDB, and more.


boto3 - helps in eastablishing base to console

Docs for AWS Boto3: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2.html

![image](https://github.com/TauqeerAhmad5201/boto3/assets/68806440/31577862-b23a-4cae-a741-fec23027fe13)

What PyPI says: 
https://pypi.org/project/boto3/

Amazon Addition: 
https://aws.amazon.com/sdk-for-python/

Example:

Hello Amazon EC2: 

import boto3

def hello_ec2(ec2_resource):
    """
    Use the AWS SDK for Python (Boto3) to create an Amazon Elastic Compute Cloud
    (Amazon EC2) resource and list the security groups in your account.
    This example uses the default settings specified in your shared credentials
    and config files.

    :param ec2_resource: A Boto3 EC2 ServiceResource object. This object is a high-level
                         resource that wraps the low-level EC2 service API.
    """
    print("Hello, Amazon EC2! Let's list up to 10 of your security groups:")
    for sg in ec2_resource.security_groups.limit(10):
        print(f"\t{sg.id}: {sg.group_name}")

if __name__ == '__main__':
    hello_ec2(boto3.resource('ec2'))
