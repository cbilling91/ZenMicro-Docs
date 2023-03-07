# Getting Started

## Visit the AWS Marketplace page for the Cost Analyzer

1. Start by browsing to the Cost Analyzer AWS Marketplace listing: <a href="https://aws.amazon.com/marketplace/pp/prodview-iedtsdptd6xje" target="_blank">ZenMicro Cost Analyzer</a>


2. Click "Continue to Subscribe"

![Alt Text](/img/marketplace.png)



3. Click "Continue to Configuration"

![Alt Text](/img/marketplace-config.png)



4. Click Choose the Cloud Formation Template you want to use.

* If you want the ZenMicro collector to be isolated in it's own network, select the "New VPC" template
* If you want the ZenMicro collector to be able to connect to other EC2 instances, select the "Existing VPC" template

![Alt Text](/img/choose-cft.png)



5. Click "Continue to Launch"

![Alt Text](/img/launch2.png)



6. Make sure "Choose Action" is set to "Launch CloudFormation" and then Click "Launch"

![Alt Text](/img/launch3.png)



7. Set the Name and Parameters for the template.

* You will need to use or create an SSH key pair to connct to the EC2 instance after launch
* The SshCIDR parameter restricts where the EC2 instance can be connected to.
    * You can restrict a connection from only your IP address using a site like https://www.whatismyip.com/. Use the Public IP Address value and append "/32". Example: 12.34.56.78/32. (Recommended)
    * You can allow connections from anywhere by setting this value to 0.0.0.0/0 which matches any IP address (Not recommended)

![Alt Text](/img/set-parameters.png)



8. Scroll to the bottom of the review page and check the box in the "Capabilities" section and click "Submit"

![Alt Text](/img/capabilities.png)



9. The template will now create the stack. This may take a few minutes.

![Alt Text](/img/complete.png)



10. Navigate to EC2 and you will see the newly launched collector instance.

![Alt Text](/img/instances.png)

NEXT: [Access the Dashboard](/Cost-Analyzer/2-Dashboard/README.md)