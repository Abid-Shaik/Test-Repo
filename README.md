
# Overview

The Teams Branded Experience (aka HOME app) and subsequent Line of Business apps allow you to quickly demonstrate the “art of the possible” and showcasing the Teams platform and articulating value that it can deliver. 

The HOME app is a personal branded landing experience which can pinned on the mobile app for Teams which consolidates information and functionality of the important 1st party and Line of Business apps that the organization wants their first line worker employees to see and work with. It can leverage multiple technologies and capabilities such as SharePoint Framework in Teams (SPFx), Graph APIs, PowerApps, Web Apps/HTML/JavaScript and mobile app pinning to light up a customer branded experience that any customer can quickly utilize and bring these experiences to life.

The HOME app was primarily designed and build as a mobile app which means not optimized for desktop view.

<table>
    <thead>
        <tr>
            <th colspan="2"> Home app Scenarios</th>
         </tr>
    </thead>
    <tbody>
        <tr>
            <td >On Shift</td>
            <td rowspan="7"><img src="data:image/png;base64,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" alt="Optional Title"></td>
         </tr>
       <tr>
            <td>Employees can view their current shift schedule and current assigned tasks under the Home tab.</td>
        </tr>
       <tr>
            <td>Employees can view the latest companywide announcements.</td>
        </tr>
       <tr>
            <td>Team members in the same shift, can chat and communicate using Teams chat.</td>
        </tr>
       <tr>
            <td>Employees can communicate and greet new team members using Teams 1:1 chat.</td>
        </tr>
       <tr>
            <td>Employees can communicate and greet new team members using Teams 1:1 chat capability. </td>
        </tr>
       <tr>
            <td>Employees can access other apps such as PayStubs and Rewards through the HOME application. </td>
        </tr>
       </tbody>
</table>

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
    * <a href="https://github.com/Abid-Shaik/Test-Repo/edit/master/README.md">Azure Service</a>
    * Azure App Service Plan
    * Application Insights
2. Microsoft Teams Shifts app enabled in Teams. Users must be a member of a team to access Shifts information.
3. Microsoft Teams Tasks app enabled in Teams. Users must be a member of a team to access Tasks information.
4. OAuth 2.0 identity provider configured for Teams. This is required to access a user’s profile information from Azure AD and Microsoft Graph.
5. Install your desired custom apps. 

![Alt text](/ReadmeImages/image.png?raw=true "Optional Title")


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

```
https://teams.microsoft.com/l/chat/0/0?users=<user1>,<user2>,...&topicName=<chat name>&message=<precanned text>
```

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













