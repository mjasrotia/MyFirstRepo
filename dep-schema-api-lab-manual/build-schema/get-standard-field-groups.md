# Get Standard Field Groups

{% hint style="info" %}
**“Field Group”** was referred as a **“mixin”** previously so these terms might be used inter- changeably
{% endhint %}

## **Identify Standard XDM Field Groups**

### **Click** on **“Step 1 - Get XDM Standard Field Groups”** API call in the “**XDM API LabCreate Schema**” Folder. E**xecute** by clicking the **“Send”** button (a sample **“GET”** call is shown below) 

**Request:**

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/2 (8).png>)

**Response**

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/3 (7).png>)

### **Search for following field groups in the Response**

Find the standard XDM field groups required for the schema. One way to find these would be to get a list of all the gloabl field groups and search for the titles below:

* Consent and Preference Details
* Personal Contact Details
* Demographic Details
* Search for following field groups in the Response\


![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/4 (2).png>)

![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/5 (3).png>)

![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/6 (3).png>)

### Copy the **“$id”** of the **above three** Field Groups and save them somewhere for future reference

{% hint style="info" %}
* Note the use of **“global”** in **https://platform.adobe.io/data/foundation/ schemaregistry/global/mixins. “global”** is used to get the XDM provided out of the box standard XDM components (Field group/mixin in this case).
* Remember we have two types of owners in AEP (Adobe/Standard and Tenant/custom).
* Adobe/Standard XDM components.
  * **https:// platform.adobe.io/data/foundation/schemaregistry/global/mixins**
* Tenant/Custom XDM Components. Note the use of tenant in place of global in the end point below:
  * **https:// platform.adobe.io/data/foundation/schemaregistry/tenant/mixins**
{% endhint %}
