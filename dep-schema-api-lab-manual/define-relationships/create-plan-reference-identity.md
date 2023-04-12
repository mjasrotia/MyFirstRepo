# Create Plan Reference Identity

## **Plan reference identity**

### **Click on “Step 4 - Reference Descriptor for Plan”** API call in the **“DEP XDM API Lab”** Folder. **Do not execute it yet.**

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/11 (3).png>)

A sample **“POST”** reference descriptor call is shown below\


<figure><img src="../../.gitbook/assets/Plan reference Identity POST.png" alt=""><figcaption></figcaption></figure>

### Make the following changes to your API call

* @type (Descriptor type) = **“xdm: descriptorReferenceIdentity**”
* xdm:sourceSchema = The **“$id”** of the **“Customer Account”** Schema.
* xdm:sourceVersion = **1** (This is always 1 as we do not maintain multiple schema versions at this point).
* xdm:sourceProperty (Full property **“path”**) = “**/\_devbc/plan/planID”**
* xdm:IdentityNamespace = **“planID”**

### Execute the **“Step 4 - Reference Descriptor for Plan”** by clicking the “Send” button

A sample API **“RESPONSE”** looks like below:

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/13 (1).png>)

{% hint style="info" %}
* You would have identified the **“relationships”** from **“Customer Account”** Schema in the **SID lab.**
* Reference Identity descriptors are created automatically from the backend when you create relationships from Schema UI. **You must create them explicitly when you create schema using API calls.**
* A reference descriptor is required to be defined for the **“Source Property”** in each lookup schema.
* A reference identity descriptor is always defined on the Source Schema where the relationship originates from (Profile in this case)
{% endhint %}

{% hint style="info" %}
**Checkpoint**

*   At this point, we created our relationships from Customer Account Schema to other lookup tables.

    * Customer to Plan relationship (M:1)&#x20;


{% endhint %}

