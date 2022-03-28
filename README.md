# Real-time email trigger
This requirement was a part of quiz(built on cloud page) where emails needed to be triggered after page is submitted - 1 mandatory and 2 conditional email triggers.
The page have multiple mandatory input fields such as first name, last name, company name.
The page also have 2 non-mandatory fields of type email.
On quiz submission we are triggering emails with the data captured in the form as personalization.
An extra field is used in email personalization - submit date.
EMAIL-A is triggered to 'xxxx@shell.com' on subission, which is a hard-coded value in our cloud page amp script.
In adition to above, if we have captured values in non-mandatory email fields then emails are triggered to those email addresses also - EMAIL-B and EMAIL-C.
Before triggering EMAIL-B and EMAIL-C we first check if it's an existing subscriber. If the subscriber already exists then trigger email to latest SubscriberID  with active status else create a new.
The responses submitted are captured in a standard data extension which is later used in EMAIL-A/EMAIL-B/EMAIL-C for personalization.
3 triggered data extensions are also in place which records the email address, subscriber key and user ID everytime EMAIL-A/EMAIL-B/EMAIL-C is triggered. Each of this triggered data extension accounts for each email send record.
