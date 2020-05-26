# PowerBIGraphCustomConnector
Power BI Graph Custom Connector

This is a sample code for a Microsoft Graph Power BI Custom Connector

You need to Register a new App in Azure and configure appropriate permissions to Graph.

- Open the Azure Portal as Admin
- Select Azure Active Directory, click Add Registrations
- Click New Registration, give a name for the App. In Redirect URI, select Web and use https://oauth.powerbi.com/views/oauthredirect.html
- Go to API Permissions, click Add Permissions, Microsoft Graph, Delegated Permissions and select all permissions you need according to the query you will execute in MS Graph.
- Click Add Permissions and then Consent.
- Go to Certificate and Secrets, click New client secret and generate a new secret for the app. Store the value generated, you will need it to configure the connector.
- Go to overview and store the value for the Application Client ID, you will need it to configure the connector.
- Close the Azure Portal


- You will need Visual Studio 2017 or 2019 to build de solution
- Install the Power Query SDK from the Visual Studio Marketplace
- Clone this repository and open MyGraph.mproj
- Open the client_id file and paste the value you have for the Application Client ID.
- Open the client_secret file and paste the value you have for the Secret.
- Build the project to produce an extension file
- Create the [My Documents]\Power BI Desktop\Custom Connectors folder
- Copy the extension file into this folder
- Open Power BI Desktop and change Data Extensions security option to allow the extension to load without any warnings
- Restart Power BI Desktop

- Open Get Data and Search for MyGraph
- Paste the Graph GET URL and load the data into Power BI

