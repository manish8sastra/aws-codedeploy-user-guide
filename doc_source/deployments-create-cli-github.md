--------

 The procedures in this guide support the new console design\. If you choose to use the older version of the console, you will find many of the concepts and basic procedures in this guide still apply\. To access help in the new console, choose the information icon\. 

--------

# Connect an AWS CodeDeploy Application to a GitHub Repository<a name="deployments-create-cli-github"></a>

Before you can deploy an application from a GitHub repository for the first time using the AWS CLI, you must first give AWS CodeDeploy permission to interact with GitHub on behalf of your GitHub account\. This step must be completed once for each application using the AWS CodeDeploy console\.

1. Sign in to the AWS Management Console and open the AWS CodeDeploy console at [https://console\.aws\.amazon\.com/codedeploy](https://console.aws.amazon.com/codedeploy)\.
**Note**  
Sign in with the same account or IAM user information that you used in [Getting Started with AWS CodeDeploy](getting-started-codedeploy.md)\.

1. On the AWS CodeDeploy menu, choose **Deployments**\.

1. Choose **Create deployment**\.
**Note**  
You will not be creating a new deployment\. This is currently the only way to give AWS CodeDeploy permission to interact with GitHub on behalf of your GitHub user account\.

1. In the **Application** drop\-down list, choose the application you want to link to your GitHub user account\.

1. In the **Deployment group** drop\-down list, choose any available deployment group\.

1. Next to **Repository type**, choose **My application revision is stored in GitHub**\.

1. Choose **Connect to GitHub**\.
**Note**  
If you see a **Connect to a different GitHub account** link:  
You might have already authorized AWS CodeDeploy to interact with GitHub on behalf of a different GitHub account for the application\.  
You might have revoked authorization for AWS CodeDeploy to interact with GitHub on behalf of the signed\-in GitHub account for all applications linked to in AWS CodeDeploy\.  
For more information, see [GitHub Authentication with Applications in AWS CodeDeploy](integrations-partners-github.md#behaviors-authentication)\.

1. If you are not already signed in to GitHub, follow the instructions on the **Sign in** page\.

1. On the **Authorize application** page, choose **Authorize application**\. 

1. Now that AWS CodeDeploy has permission, choose **Cancel**, and continue with the steps in [Create an EC2/On\-Premises Compute Platform Deployment \(CLI\)](deployments-create-cli.md)\.