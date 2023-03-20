# Create Schema

## 1. Click on **“Step 3 - Create Customer Account Schema”** API call in the “**XDM API LabCreate Schema**” Folder. **Do not execute it yet**



<figure><img src="../../.gitbook/assets/create CA schema API highlight.png" alt=""><figcaption></figcaption></figure>

* A Sample payload for creating a Schema looks like this.

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/15 (5).png>)

* Change the **“title”** and **“description”** in your schema payload
  * Title: **“Sample Customer Schema - \<your Sandbox number>”**
  * Description: **“Sample Customer Schema - \<your Sandbox number>”**
  * In real world, the title and description should be very carefully defined.
* Make sure you have the right “$id” values for the field groups you are including in the schemas. You copied the “id” of the required field group in the steps “**5.d**” and “**6.e**” above.
* Execute **“Step 3 - Create Customer Account Schema”** by clicking the **“Send”** button
* A sample response of a **“POST”** Schema call looks like the below.

<figure><img src="../../.gitbook/assets/create CA Schema API response.png" alt=""><figcaption></figcaption></figure>

## 2. Copy the “$id” and “meta:altId” to use for future references to “Customer Account” Schema. Keep this copied IDs handy in a notepad as they will be required for future reference in further steps.



{% hint style="info" %}
**Notes**:

* A Schema must include a **“Class”** and a possible **“Field Group”.** This schema would be created by combining
  * **“XDM Individual Profile”** Class
  * **“Demographic Details”** Field Group
  * **“Personal Contact Details”** Field Group
  * **“Consent and Preference Details”** Field Group
  * “**Customer Account Details**” Custom Field Group
* Each Schema must have a **“title”** and a **“description”.**
* Notice the use of **“devbc”** in the API response below which is the tenant namespace assigned to your IMS Org.
{% endhint %}



{% hint style="info" %}
**Checkpoint**

* At this point, we created our schema successfuly using
  * Profile Class
  * Required Field groups
    * Standard
    * Custom
{% endhint %}

****
