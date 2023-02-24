# Week 0 — Billing and Architecture

## TASK | COMPLETED:



| CATEGORY | TASK | COMPLETED | OUTPUT | 
| --- | --- | --- | --- |
| Video | Streamed class | :heavy_check_mark: | :heavy_check_mark: |
| | Chirag - Spend Considerations | :heavy_check_mark:  | :heavy_check_mark: |
| | Ashish - Security Considerations | :heavy_check_mark:  | :heavy_check_mark: |
| Hands-on | Recreate Conceptual Diagram | :heavy_check_mark: | :heavy_check_mark: |
| | Recreate Logical Diagram | :heavy_check_mark: | :heavy_check_mark: |
| AWS | Create an Admin User | :heavy_check_mark: | :heavy_check_mark: |
| | Use CloudShell | :heavy_check_mark: | :heavy_check_mark: |
| | Generate AWS Credentials | :heavy_check_mark: |:heavy_check_mark: |
| | Installed AWS CLI | :heavy_check_mark: |:heavy_check_mark:  |
| | Create a Billing Alarm | :heavy_check_mark: | :heavy_check_mark: |
| | Create a Budget | :heavy_check_mark: | :heavy_check_mark: |




## I Generated AWS Credentials|

## Architecture Diagram

I Recreated Logical Architectual Diagram in Lucid Charts

I Recreated Conceptual Diagram in Lucid Charts or on a Napkin

maayaa06 (Sharon Sekyere): [Conceptual and Logical Diagram](https://lucid.app/lucidchart/110e6690-4013-4f7c-97f6-492366c3fc82/edit?invitationId=inv_e8818191-7dd1-4afa-b61c-4d075528a485&page=0_0#)


## I Created an Admin User

I first created a root account with MFA initialized. 
On the Console Home page, selected the IAM service.
In the navigation pane, selected Users and then selected Add users.
On the Specify user details page, under User details, in User name, entered the name for the new user as maayaap.

Selected Provide user access to the – AWS Management Console.
created user credentials and
selected Download .csv to download the user's sign in credentials as a .csv file to save to a safe location.
 
Created a password for the user and
granted user admin permissions.
Configured multi-factor authentication (MFA) for the user.
Gave users permissions to manage their own security credentials.

Selected Email sign-in instructions. 

•	User name

•	URL to the account sign-in page. Used the following example, substituting the correct account ID number or account alias:
https://AWS-account-ID or alias.signin.aws.amazon.com/console

Then clicked create user.





## installed AWS CLI

i did the following steps to install AW CLI.

I installed AWS CLI via gitpod

!.[Installing AWS CLI](assets/)

```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

## Created a Billing Alarm

In creating a billing alarm i did the following steps:

Logged onto my AWS IAM user account and
signed into AWS management console.
navigated the billing and cost managemnt dashboard and
clicked on billing preferences.
Viewed options stating either by pdf invoice or email.
Chose receive billing alerts and Receive Free Tier Usage Alerts.
Entered my email and click save preferences.

further on the left side of the page clicked on Create Alarm.
Clicked Select metric.
After that clicked Billing and then Total estimated charge.
chose currency as USD and clicked  select metric button.
chose conditions to trigger the alarm. 
Selected the threshold type as Static.
Then for an alarm condition, choose, “Greater”. 
Finally, entered the threshold value for my bill.
 keept it at 1$. 
 Click on the Next button.
Entered the Alarm name
clicked on the “Create alarm” button at the bottom of the screen.


## created a budget
 created  a  budget using AWS CLI 


