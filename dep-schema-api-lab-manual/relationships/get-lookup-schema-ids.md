# Get Lookup Schema IDs

## Get Lookup Schemas&#x20;

### **Execute the “Step 1 - Get Lookup Schemas”** API call in the **“DEP XDM API Lab”** Folder.

The provided GET call fetches all the schemas but we only need to search the schemas we are using for our lookups. For example, “Plan” schema is used as a lookup for Customer Account which holds all the plan related information.

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/2 (9).png>)

Within your response look for the Plan Schema (Search keyword “**dep: Lookup Plan**”)

A sample **“GET”** schema call is shown below

![Graphical user interface, text, application, email

Description automatically generated](../../.gitbook/assets/3.jpeg)

A Sample API **“RESPONSE”** looks like below (Search for Plan Schema):

![Graphical user interface, application

Description automatically generated](../../.gitbook/assets/4.jpeg)

### Copy the **“$id”** of this schema and paste it somewhere you can access later. It will be required in future relationship descriptor API calls.

{% hint style="info" %}
* This schema should be pre-deployed on your Sandbox.
* Relationship Descriptors will be created from Customer Account schema to this lookup schema.
{% endhint %}

##
