
# Overview

The Teams Branded Experience (aka HOME app) and subsequent Line of Business apps allow you to quickly demonstrate the “art of the possible” and showcasing the Teams platform and articulating value that it can deliver. 

The HOME app is a personal branded landing experience which can pinned on the mobile app for Teams which consolidates information and functionality of the important 1st party and Line of Business apps that the organization wants their first line worker employees to see and work with. It can leverage multiple technologies and capabilities such as SharePoint Framework in Teams (SPFx), Graph APIs, PowerApps, Web Apps/HTML/JavaScript and mobile app pinning to light up a customer branded experience that any customer can quickly utilize and bring these experiences to life.

The HOME app was primarily designed and build as a mobile app which means not optimized for desktop view.

|              Stage | Direct Products | ATP Yields |
| -----------------: | --------------: | ---------: |
|         Glycolysis |           2 ATP |            |
|                 ^^ |          2 NADH |   3--5 ATP |
| Pyruvaye oxidation |          2 NADH |      5 ATP |
|  Citric acid cycle |          2 ATP              ||
|                 ^^ |          6 NADH |     15 ATP |
|                 ^^ |          2 FADH |      3 ATP |
|                                   30--32 ATP    |||



| Attempt | #1 | #2 |
| :---: | :---: | :---: |
| Seconds | 301 | 283 |
| Seconds | 301 | 283 |


# Solution overview

## Prerequisites

1. An Azure Active Directory (Azure AD) subscription and the following resources:
    * Azure Service
    * Azure App Service Plan
    * Application Insights
2. Microsoft Teams Shifts app enabled in Teams. Users must be a member of a team to access Shifts information.
3. Microsoft Teams Tasks app enabled in Teams. Users must be a member of a team to access Tasks information.
4. OAuth 2.0 identity provider configured for Teams. This is required to access a user’s profile information from Azure AD and Microsoft Graph.
5. Install your desired custom apps. 

-----------Image----------

## Authentication and Single Sign on (SSO)

The HOME app authentication flow is based on user profile information stored in Azure AD and accessed using Microsoft Graph. 


The Teams Single Sign-on API is currently supported in Teams Developer Preview and will be available to the general public soon.

Learn more about authentication for Microsoft Tabs and SSO in Teams: 

## HOME Web App: 

HOME app is a .Net (v2.4) core MVC Web Application which uses AADID for authentication and integrates nicely with other LOB apps through Teams deep-links
## Technical aspects
1. .Net core MVC web app (v2.4)
2. Microsoft Graph API for Shifts, Tasks, User profile information
3. Azure Active Directory Identity authentication 
4. Microsoft SharePoint Framework (v1.10) in Teams
5. App Template (Company communicator)
6. Microsoft Power Apps

## Capabilities overview
1. HOME app is an ASP.NET Core MVC application.
2. Access employee Shifts schedules using Microsoft Teams Shifts Graph API integration.
3. Display employee tasks using Microsoft Planner Tasks Graph API integration.
4.Customize HOME app to create a tailored experience. For example, the announcement feature of the HOME app can be integrated with our Company Communicator app template to share your company’s the information and notifications within the HOME app.
5. Retrieve a list of team members in the same shift by using the Microsoft Graph List Members API.
6. Enhance the user chat experience by creating deep links to private chats within the HOME app.
7. The Microsoft Graph photo API can be called to display a team member’s user profile picture. 
8. Get user profile information using the Microsoft Graph Get User API. 

## On/off shift switch

On/Off shift switch is controlled by employees’ shift schedule. If there is no shift scheduled for the time of HOME app access, then the experience will be off shift. See scenario # 6.

## Microsoft Teams Shifts integration (Graph API): 
 
Employees’ shift schedule display is pulled using Microsoft Teams Shifts Graph API integration. 


Use below link to view Graph API documentation for Microsoft Shift:
https://docs.microsoft.com/en-us/graph/api/schedule-list-shifts?view=graph-rest-1.0&tabs=http

## Microsoft Teams Tasks integration (Graph API): 
Display tasks which is assigned to a login employee, using Microsoft Planner tasks Graph API.
Link to Microsoft Graph API Planner tasks documentation:
https://docs.microsoft.com/en-us/graph/api/planneruser-list-tasks?view=graph-rest-1.0&tabs=http

## Announcements/Company communicator integration (App Template)
The announcement section of the HOME app could be the Teams Company communicator app template. Using company communicator app template, you can share latest announcement information in the HOME app. 

Here are Company communicator documentation and repository links: 

https://docs.microsoft.com/en-us/microsoftteams/platform/samples/app-templates#company-communicator-app

https://github.com/OfficeDev/microsoft-teams-company-communicator-app

### How to integrate company communicator into HOME app? 

1. Read Microsoft Azure storage table using:
REST API- https://myaccount.table.core.windows.net/MyTable()  

2. Get the Table service SAS by going through the Shared Access Token section.
3. Ensure to set the StorageTableEndPoint value in appsettings. json in the below format.

https://myaccount.table.core.windows.net/MyTable()?<Table service SAS URL>  

Learn more here: 
https://docs.microsoft.com/en-us/rest/api/storageservices/querying-tables-and-entities

### Group and 1:1 chat integration (Graph API)- Working now chat/ new team members greeting: 

#### Team members:
Get a list of team members in the same shift by using “List member” Graph API. 
https://docs.microsoft.com/en-us/graph/api/group-list-members?view=graph-rest-1.0&tabs=http

Deep linking has been used for the Chat integration, kindly use the below format for deep linking to a chat

https://teams.microsoft.com/l/chat/0/0?users=<user1>,<user2>,...&topicName=<chat name>&message=<precanned text> ---------------------> need to change

Please go through the below link for more information on deep linking.

https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/deep-links#generating-a-deep-link-to-a-chat

#### profile picture:
To display user profile picture of the team member use profile photo Graph API.
https://docs.microsoft.com/en-us/graph/api/profilephoto-get?view=graph-rest-1.0

#### User details:
To retrieve the user profile information, use “Get a user” Graph API.

https://docs.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0&tabs=http

#### Custom Apps integration:

HOME app source code comes with sample custom apps such as Paystub and Rewards.
There are placeholders in the source code for other custom apps such as News, etc. to showcase Microsoft Teams platform capabilities in HOME app. You can replace sample custom apps with other apps as you require.

Each custom app needs to be created separately and installed into Microsoft Teams as a standalone installation.
 
Below is the instruction to create and integrate Paystub and Rewards sample custom apps along with other SharePoint Framework (News) and Power Apps, into the HOME app.

### Paystubs and Rewards sample custom apps:
Paystubs and Rewards custom app source code is included in the HOME app solution. Use the manifests to deploy the applications into Teams.

#### Paystub manifest:

------image -----

#### Rewards manifest:

------image -----

##### Other sample custom apps
Below custom apps are not included in HOME app source code solution. Follow the instruction to create and integrate SharePoint Framework such as News or any Power Apps into HOME app. 













