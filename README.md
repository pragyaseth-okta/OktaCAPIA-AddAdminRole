# Using Custom API Action to Add Okta Admin Role to User

Overview
File download: 

The workflow allows automated management of help desk role within Okta. The flow leverages Okta's Custom API action which can be used to invoke any of Okta's published APIs. This sample flow uses a custom 'Role' attribute as part of Okta user profile. If user is created with a 'Support' role, user is added to HELP_DESK_ADMIN role. 

Prerequisites
Before you get started, here are the things you’ll need:

Access to an Okta tenant with Okta Workflows enabled for your org
Custom 'Role' attribute created on Okta's default user profile

Setup Steps
Select the “Add User to Admin Role” flow from the folder.
If you have not already done so, authorize the connections to Okta.
Click Save. Be sure to select “Save All Data.”
In the top toolbar of the Workflow console, toggle the “Flow is OFF” switch to “ON”

Testing this Flow
Create a user in your Okta tenant using Okta 'Create User' API with the profile attribute "role" set as "Support" in the request body.
Open your flow and view Flow History. You should see a successful flow run.
Go to Okta admin console and review the list of administrators under Security -> Administrators tab.
You should see the newly created user listed with 'Help Desk Admin' role.

Limitations & Known Issues
If extending this flow to work with other Okta events, please note that only a subset of System Log events are available in the Okta connector.
