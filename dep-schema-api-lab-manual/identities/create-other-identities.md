# Create Other Identities

## **Click on “Step 2 - Create Email Address Identity for Customer Account Schema”** API call in the **“XDM API Lab Create Identity Descriptors”** Folder. **Do not execute it yet.**

![Graphical user interface, text, application, email

Description automatically generated](../../.gitbook/assets/5.png)

* A sample **“POST”** schema descriptor call looks like below.

![Graphical user interface, text, application, email

Description automatically generated](../../.gitbook/assets/6.png)

* Make the following changes to the API call.
  * @type (Descriptor type) = **“xdm:descriptorIdentity**”
  * xdm:sourceSchema = The **“$id”** of the **“Customer Account”** Schema.
  * xdm:sourceVersion = **1** (This is always 1 as we do not maintain multiple schema versions at this point).
  * xdm:sourceProperty (Full property **“path”**) = “**/personalEmail/address”**
  * xdm:namespace ( Identity **“namespace”) = “Email”**
  * isPrimary = **“false”**
* A Sample API **“RESPONSE”** looks like below:

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/7 (7).png>)

* Execute **“Step 2 - Create Email Address Identity for Customer Account Schema”** by clicking the **“Send”** button

{% hint style="info" %}
**Notes:**

* You would have identified the remaining Identities for **“Customer Account”** Schema in the SID lab.
* You can have more than 1 non-Primary person identities for a Schema if they are valid and do not create collisions across different individuals
{% endhint %}



{% hint style="info" %}
**Checkpoint**

* At this point, we marked the required Identities
  * Primary Identity
  * Non-Primary Identities (Required for Lookups)
{% endhint %}
