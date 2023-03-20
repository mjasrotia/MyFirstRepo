# Get Standard Field Groups

{% hint style="info" %}
**Notes**

**“Field Group”** was referred as a **“mixin”** previously so these terms might be used inter- changeably
{% endhint %}

**1. Click** on **“Step 1 - Get XDM Standard Field Groups”** API call in the “**XDM API LabCreate Schema**” Folder. E**xecute** by clicking the **“Send”** button (a sample **“GET”** call is shown below)\



* **Request:**

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/2 (8).png>)

* **Response**

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/3 (7).png>)

## **2. Search for following field groups in the Response**

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

## 3. Copy the **“$id”** of the **above three** Field Groups and save them somewhere for future reference

{% hint style="info" %}
**Note:**

* Note the use of **“global”** in **https://platform.adobe.io/data/foundation/ schemaregistry/global/mixins. “global”** is used to get the XDM provided out of the box standard XDM components (Field group/mixin in this case).
* Remember we have two types of owners in AEP (Adobe/Standard and Tenant/custom).
* Adobe/Standard XDM components.
  * **https:// platform.adobe.io/data/foundation/schemaregistry/global/mixins**
* Tenant/Custom XDM Components. Note the use of tenant in place of global in the end point below:
  * **https:// platform.adobe.io/data/foundation/schemaregistry/tenant/mixins**
{% endhint %}
