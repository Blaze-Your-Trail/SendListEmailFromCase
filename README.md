# SendListEmailFromCase
Allows users to email multiple contacts from the Case List View using Custom Labels to identify the Email Template Folder
Create a List button on the Case Object and add the Visual Force Page as the Content Source
Go to Setup -> Custom Label --> New Custom Label - you need to create 2 custom labels
First Custom Label is for the Email Template Folder Name
Short Description and Name are EmailTemplateFolderID
Value = "Name of your folder" (Find the folder in your Classic Email Templates in Set Up). Save.
Second Custom Label is for the Email Template itself (required for testing)
Find the Email Template and take the ID from the URL - drop the 2F at the front (this denotes a foward slash)
Add this ID to the Value field. Save
Create the Send List Email Button (after you create the Visual Force Page in Sandbox)
SELECT Id, Address FROM OrgWideEmailAddress where Address ='requests@babygiveback.org'
