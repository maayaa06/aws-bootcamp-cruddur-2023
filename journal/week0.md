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



## Architecture Diagram

I Recreated Logical Architectual Diagram in Lucid Charts

maayaa06 (Sharon Sekyere): [Conceptual and Logical Diagram](https://lucid.app/lucidchart/110e6690-4013-4f7c-97f6-492366c3fc82/edit?invitationId=inv_e8818191-7dd1-4afa-b61c-4d075528a485&page=0_0#)


### Create a new User and Generate AWS Credentials

• Created a root account with MFA enabled.

• On the Console Home page, selected the IAM service.

• In the navigation pane, selected Users and then selected Add users.

• On the Specify user details page, under User details, in User name, entered the name for the new user as maayaap.

• Selected Provide user access to the – AWS Management Console.

• created user credentials and

• selected Download .csv to download the user's sign in credentials as a .csv file to save to a safe location.
 
• Created a password for the user and

• granted user admin permissions.

• Configured multi-factor authentication (MFA) for the user.

• Gave users permissions to manage their own security credentials.

Selected Email sign-in instructions. 

•	User name

•	URL to the account sign-in page. Used the following example, substituting the correct account ID number or account alias:
https://AWS-account-ID or alias.signin.aws.amazon.com/console

Then clicked create user.




## installed AWS CLI

I did the following steps to install AW CLI:

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

created second billing alarm for monthly usage at 5$


## created a Budget

I did the following steps in creating budget:
    
    
 ## 1.Contents of budget.json:
    
    {
    "BudgetLimit": {
        "Amount": "1",
        "Unit": "USD"
    },
    "BudgetName": "Example Tag Budget",
    "BudgetType": "COST",
    "CostFilters": {
        "TagKeyValue": [
            "user:Key$value1",
            "user:Key$value2"
        ]
    },
    "CostTypes": {
        "IncludeCredit": true,
        "IncludeDiscount": true,
        "IncludeOtherSubscription": true,
        "IncludeRecurring": true,
        "IncludeRefund": true,
        "IncludeSubscription": true,
        "IncludeSupport": true,
        "IncludeTax": true,
        "IncludeUpfront": true,
        "UseBlended": false
    },
    "TimePeriod": {
        "Start": 1477958399,
        "End": 3706473600
    },
    "TimeUnit": "MONTHLY"
}


## 2.Contents of notifications-with-subscribers.json:



    {
        "Notification": {
            "ComparisonOperator": "GREATER_THAN",
            "NotificationType": "ACTUAL",
            "Threshold": 80,
            "ThresholdType": "PERCENTAGE"
        },
        "Subscribers": [
            {
                "Address": "m16430347@gmail.com",
                "SubscriptionType": "EMAIL"
            }
        ]
    }
]


## 3.create-budget

aws budgets create-budget \
    --account-id  \
    --budget file://aws/budget.json \
    --notifications-with-subscribers file://aws/notifications-with-subscribers.json
