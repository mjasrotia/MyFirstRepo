# Browse Identities through API

## Get Customer Account Schema

### Click on **“Step 3 - Get Customer Account Schema and its descriptors”** API call in the **“XDM API Lab Create Identity Descriptors”** Folder. **Do not execute it yet.**

![Graphical user interface, text, application, email

Description automatically generated](../../.gitbook/assets/8.png)

A sample **“GET”** schema call is shown below\


![](<../../.gitbook/assets/9 (5).png>)

### Validate/modify your API call. Replace **“meta:altId”** with your schema’s “meta:altID”

### Execute **“Step 3 - Get Customer Account Schema and its descriptors”** by clicking the “Send” button.

A sample API **“RESPONSE” is provided below**

![Graphical user interface, text, application

Description automatically generated](<../../.gitbook/assets/10 (4).png>)

Browse further down in the API response to see the Identity Descriptors for this Schema.

![Text

Description automatically generated](<../../.gitbook/assets/11 (5).png>)

{% hint style="info" %}
* Observe the changed “Accept” header in this case. This “accept “ header will return the Schemas along with its associated descriptors in the API response.
* You can see other **“Accept”** header options here [**Schema Registry APIs**](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/overview.html?lang=en)
  * With the pre-loaded Accept Header in the postman collection, you will see the fully exploded hierarchical view of the “Customer Account” Schema where every single property belonging to a class, or a field group will be returned.
* All the object properties will be exploded all the way to their leaf nodes.
{% endhint %}

##
