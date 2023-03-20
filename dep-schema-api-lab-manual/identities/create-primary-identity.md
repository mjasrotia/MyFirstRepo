# Create Primary Identity

## 1.  **Click on “Step 1 - Create Primary Identity for Customer Account Schema”** API call in the **“XDM API Lab Create Identity Descriptors”** Folder. **Do not execute it yet.**

![Graphical user interface, text, application, email

Description automatically generated](../../.gitbook/assets/2.png)

* A sample **“POST”** schema descriptor call looks like below.

![](<../../.gitbook/assets/3 (1).png>)

* **Make the following changes to the API call.**
  * @type (Descriptor type) = **“xdm:descriptorIdentity**”
  * xdm:sourceSchema = The **“$id”** of the **“Customer Account”** Schema.
  * xdm:sourceVersion = **1** (This is always 1 as we do not maintain multiple schema versions at this point).
  * xdm:sourceProperty (Full property **“path”**) = “**/\_devbc/customerID”**
  * xdm:namespace ( Identity **“namespace”) = “customerID”**
  * isPrimary = **“true”**
* Execute **“Step 1 - Create Primary Identity for Customer Account Schema”** by clicking the “Send” button
* A sample API **“RESPONSE”** looks like below:

![Graphical user interface, text, application, email

Description automatically generated](../../.gitbook/assets/4.png)

{% hint style="info" %}
**Notes:**

* You would have identified the **“Primary”** Identity for “Customer Account” Schema in the SID lab.
* Note the use of **“descriptors”** in **https://platform.adobe.io/data/foundation/ schemaregistry/tenant/descriptors.**
{% endhint %}

****
