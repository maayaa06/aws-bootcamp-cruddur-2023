# Week 0 — Billing and Architecture


## TASK | COMPLETED |

|  --- |    ---    |

| I Watched Live - Streamed Video |

| Watched Chirag's - Spend Considerations   |

| Watched Ashish's - Security Considerations |


## I Generated AWS Credentials|

## Architecture Diagram

I Recreated Logical Architectual Diagram in Lucid Charts

I Recreated Conceptual Diagram in Lucid Charts or on a Napkin

maayaa06 (Sharon Sekyere): [Conceptual and Logical Diagram](https://lucid.app/lucidchart/110e6690-4013-4f7c-97f6-492366c3fc82/edit?invitationId=inv_e8818191-7dd1-4afa-b61c-4d075528a485&page=0_0#)


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

Logged onto my AWS IAM user account
signed into AWS management console
navigated the billing and cost managemnt dashboard
clicked on billing preferences
Viewed options stating either by pdf invoice or email
Chose receive billing alerts and Receive Free Tier Usage Alerts.
Entered my email and click save preferences.

further on the left side of the page clicked on Create Alarm
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


## I Created an Admin User

i first created a root account with MFA initialized. Then from IAM dahboard in my root account 
