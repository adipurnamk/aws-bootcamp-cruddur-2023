# Week 0 — Billing and Architecture

## Logical Architectual Diagram in Lucid Charts
https://lucid.app/lucidchart/f66a78bf-14fd-40d8-a1fc-e65645e223aa/view?page=0_0&invitationId=inv_c5c78108-6652-4ae0-8b97-3dae65bd2cae#

---

## Security Consideration
## Create an Admin User
From Search Bar, search for IAM to make a new Admin user.	
![IAM](./week0/admin/1.png)
Insert desired Admin User name.
![User Name](./week0/admin/2.png)
Choosing permission, for the best practice we'll make a new 'admin group', set permission and add new admin user into this group.
![Permission](./week0/admin/3.png)
Make a new group with defined administrator permission.
![Make New Admin Group](./week0/admin/4.png)
Choose created group to our admin user.
![Select Creted Group](./week0/admin/5.png)
Add tag for better audit.
![Tag](./week0/admin/6.png)
Finished. An Admin User has been created.
![Finished](./week0/admin/7.png)

## Use CloudShell	
To open AWS Cloudshell, you can click Terminal icon on the left side of notification icon, on the top bar.
![AWS Cloudshell](./week0/cloudshell/1.png)
Welcome to AWS Cloudshell!
![AWS CLoudshell Welcome Page](./week0/cloudshell/2.png)
If you facing "Unable to start the environment. To retry, refresh the browser or restart by selecting Actions, Restart AWS CloudShell." error. Please refer this [documentation](https://repost.aws/questions/QUH54A371dRvej5J1G_yZogw/error-when-launching-aws-cloud-shell-unable-to-start-the-environment) and change your region.
![Unable to start the environment](./week0/credentials/1.png)

## Generate AWS Credentials
### Generate Console Access
To enable Console Access, you can click Enable Console Access in IAM > User > Security credentials tab.
![Enable Console Access](./week0/credentials/1.png)
Set your preference, choose Enable console access. 
![Manage Console Access](./week0/credentials/2.png)
Download .csv.
![Password](./week0/credentials/3.png)

### Generate AWS CLI Access
To enable AWS CLI, AWS Tools for PowerShell, AWS SDKs, or direct AWS API calls, you can click Enable Console Access in IAM > User > Security credentials tab.
![Enable Access](./week0/credentials/4.png)
Choose Command Line Interface (CLI).
![Choosing](./week0/credentials/5.png)
Add tag by your preference.
![Tags](./week0/credentials/6.png)
Download .csv.
![Download](./week0/credentials/7.png)

## Install AWS CLI
We need to install AWS CLI first. Since I'm using Ubuntu (WSL based), we'll install based on [Installing or updating the latest version of the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

![Download .zip ](./week0/cli/1.png)
Check AWS CLI installation using 'aws --version' command.
![AWS CLI Version](./week0/cli/2.png)
Configure AWS CLI using 'aws configure' and check running configuration using 'aws configure list'.
![AWS Configure](./week0/cli/3.png)

## Create a Billing Alarm	
## Create a Budget	

---

## Challange
