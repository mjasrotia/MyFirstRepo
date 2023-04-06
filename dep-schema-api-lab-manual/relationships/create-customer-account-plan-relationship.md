# Create Customer Account - Plan Relationship

## Customer Plan Relationship

### **Click on “Step 2 - Relationship Descriptor Customer Account To Plan”** API call in the **“DEP XDM API Lab”** Folder. **Do not execute it yet.**

![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/5 (1).png>)

A sample **“POST”** relationship descriptor call is shown below

![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/6 (6).png>)

### **Make the following changes to the API call.**

* @type (Descriptor type) = **“xdm: descriptorOneToOne**”
* xdm:sourceSchema = The **“$id”** of the **“Customer Account”** Schema.
* xdm:sourceVersion = **1** (This is always 1 as we do not maintain multiple schema versions at this point).
* xdm:sourceProperty (Full property **“path”**) = “**/\_devbc/plan/planID”**
* xdm:destinationSchema = The **“$id”** of the **“Plan lookup”** Schema.
* xdm:destinationVersion = **1** (This is always 1 as we do not maintain multiple schema versions at this point).

### Execute **“Step 2 - Relationship Descriptor Customer Account To Plan”** by clicking the “Send” button

A sample API **“RESPONSE”** is shown below

<figure><img src="../../.gitbook/assets/customer to plan relationship descriptor response.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
* You would have identified the **“relationships”** for **“Customer Account”** Schema in the **SID lab**.
* **“Customer Account** : **Plan**” relationship cardinality is “**M:1**” .
* A relationship descriptor is always defined from either the **“Profile”** or the **“Experience Event”** class-based schemas (Profile class in this case).
* It’s worth noting that AEP only supports **1 hop join** from Profile or Experience Event schemas i.e. we can only create **1 level lookup** relationships.
* Even though the descriptor type refers to **OneToOne** , we use this to define relationships for **M:1 cardinality** in AEP.
{% endhint %}

