# Modify Schema - JSON Patch

## 1. **Schema Modification requirement**

* Assume we forgot to add a custom field **“planDescription”** under \_**devbc==>plan** object in Customer Account Schema. UI Schema screen shot below shows that.

![Graphical user interface, application

Description automatically generated](../../.gitbook/assets/0.png)

* While using APIs, we can use a JSON PATCH call to update a portion of the schema. More information about JSON patch is here
  * [**http://jsonpatch.com/**](http://jsonpatch.com/)****
  * **https://experienceleague.adobe.com/docs/experience-platform/xdm/api/ schemas.html#patch**
* Remember the following points.
  * In AEP, a schema is composed of a class and a set of 1 or more field groups.
  * We cannot add properties directly to a schema without adding it first to a field group. This helps in re-usability of a field group across schemas.
* To add a new property to a schema, you would need to follow the below steps.
  * Identify the field group where you would like to add the new property
  * Construct a JSON-PATCH call to update the field group.
  * Execute the JSON-PATCH API call to update the Field group (which the schema will inherit)

## **2. Get the fully qualified path for the schema object you need to update**

* **Execute the “Step 1 - Get Tenant Field groups”** under **“XDM API Lab Customize Schema”** folder **** by clicking the **“Send”** button

![Graphical user interface, text, application

Description automatically generated](../../.gitbook/assets/1.png)

* Search for the schema ID for the custom field group using the display name from UI. Copy the **“meta:altId”** . This will be used in the next step to execute the PATCH call against this field group.\


![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/2 (5).png>)

* **Execute the “Step 2 - Fetch path for the object to be modified”** under **“XDM API Lab Customize Schema”** folder **** by clicking the **“Send”** button
* Get the fully qualified JSON path for the object which needs to be updated. In this case, you will have to get the path for the “plan” object. /definitions/customFields/properties/\_devbc/properties/plan/properties

![A picture containing graphical user interface

Description automatically generated](<../../.gitbook/assets/3 (5).png>)

* **Click on “Step 3 - Modify Tenant Field group”** API call in the **“XDM API Lab Customize Schema”** Folder. **Do not execute it yet.**

****

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/4 (5).png>)

* A sample **“PATCH”** call is shown below
  * We are using the **“add”** operation here as we are adding a new property
  * Make sure that the fully qualified path is correctly specified.
  * The API request should be having the exact schema ID of the field group we are updating.

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/5 (10).png>)

* A sample API **“RESPONSE”** is shown below
  * First screen shot shows that the “$id” of the schema does not change as we are updating an existing schema
  * Second screen shot below validates that the new property “name” is added to the schema.

![Timeline

Description automatically generated](<../../.gitbook/assets/6 (11).png>)

![Graphical user interface

Description automatically generated](<../../.gitbook/assets/7 (10).png>)

* Execute the **“Step 3 - Modify Tenant Field group”** by clicking the “Send” button

## **3. Browse your Schema through the UI and have a look at your newly added property**

* See the additional property added to the “plan” object below

![Graphical user interface, application

Description automatically generated](<../../.gitbook/assets/8 (6).png>)
