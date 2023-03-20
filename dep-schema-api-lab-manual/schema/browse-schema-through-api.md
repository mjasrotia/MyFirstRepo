# Browse Schema through API

## Execute **“Step 5 - Get Customer Account Schema”** API call by clicking the “Send” button.

* A sample **“GET”** schema descriptor is shown below\


<figure><img src="../../.gitbook/assets/Get CA Schema using meta altID.png" alt=""><figcaption></figcaption></figure>

* Replace the meta:altID in your API call with your “Customer Account” schema’s “meta:altID”.
* A sample API **“RESPONSE”** looks like below:

![Timeline

Description automatically generated](<../../.gitbook/assets/19 (1).png>)

{% hint style="info" %}
**Notes:**

* Note the use of **“tenant”** in **https://platform.adobe.io/data/foundation/ schemaregistry/tenant/mixins.**
* Note the use of **“tenant”** in **https://platform.adobe.io/data/foundation/ schemaregistry/tenant/mixins.**
* Observe the use of “meta:altId” to fetch the Schema from the registry. Replace the meta:altID in your API with the meta:altID of the Customer Account Schema.
* Also observe the “Accept” header which tells the schema registry what to return in the API Response. You can see other “Accept” header options here [**Schema**](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/overview.html?lang=en) **** [**Registry APIs**](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/overview.html?lang=en)
* With the pre-loaded Accept Header, you will see the fully exploded hierarchical view of the Customer Account Schema where every single property belonging to a class or a field group will be exposed.
* All the object properties will be exploded all the way to their leaf nodes.
{% endhint %}
