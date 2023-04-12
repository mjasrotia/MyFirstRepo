# Generate Access Token

## API Security Overview

To establish a secure service-to-service Adobe API session, Adobe requires you to create a JSON Web Token (JWT) that encapsulates the identity of your developer project integration, and then exchange it for an access token. A developer project integration can only be created by those with `Developer Rights` and is assigned within the Adobe Admin Console at a product level. Once you have these rights you can create developer projects utilizing the various Adobe product related APIs.  This is where creating a JWT comes into the picture.  To create a JWT you must' pass a certain set of claims to Adobe's Identity Management Service (IMS) and those claims must be signed using a valid digital signing certification (i.e. public/private key pair).

{% hint style="info" %}
You can learn more about this process [here](https://developer.adobe.com/developer-console/docs/guides/authentication/JWT/) but for the bootcamp we will "hand wave" this step of the process and instead utilize a super neat Postman library
{% endhint %}

Every request to any Adobe service must include the access token in the Authorization header along with the Client Secret that was generated during the developer project creation.  Additionally, the Experience Platform and its associated applications require two other header params are present on each request.&#x20;

* `x-gw-ims-org-id` - this param specifies the `IMS Org` that the request belongs to and ensures the processing of the requests resolves to the appropriate SaaS environment
* `x-sandbox-name` - this param specifics which sandbox to process the request in within the Experience Platform

{% hint style="danger" %}
Not specifying the `x-sandbox-name` param does not fail the request as you might expect. Instead it defaults the request to process into the `default` sandbox that is automatically provisioned with any Experience Platform environment
{% endhint %}

{% hint style="info" %}
As part of this bootcamp we created a developer project and provided you a Postman Environment file with all of the necessary values to create a JWT and request an `access_token` .  This is what you uploaded in the previous steps of the lab
{% endhint %}



## Postman + Adobe IMS

As discussed above, to be able to utilize Adobe product API's you must include and access token in the Authorization header of each request. Adobe has developed a request in Postman that locally signs the JWT on your machine and then passes that JWT in the call to Adobe's Identity Management Service (IMS) to authenticate. To locally sign the JWT a crypto JavaScript library is loaded as part of a pre-request script in the Postman request. This script uses the “RSA-Sign JavaScript Library” and creates a Global Postman environment variable (which persists even if you close Postman, nice!).&#x20;

You can see the code for this request within the `AEP Foundations Bootcamp` collection under the calls `Pre-request Scripts` tab within the call itself.

<figure><img src="../../.gitbook/assets/bootstrapping-auth.png" alt=""><figcaption><p>Bootstrapping the Adobe Authentication Process Using Postman</p></figcaption></figure>

Now that you understand a little bit about how Adobe secures its API's and what is required to work them lets actually use them.



## Authenticate with Postman

1. Launch Postman and navigate to the directory titled `IMS Authenticate` and open the request by clicking on it
2. Next in the upper right corner of Postman you'll see an environment drop-down. Select the `AEP Bootcamp` environment from the drop-down
3. Now execute the call by clicking the “Send” button

![](<../../.gitbook/assets/14 (1).png>)

A successful response should look like this





## Common Errors

### **Invalid Token**

This occurs when the `private_key` in your environment file is malformed or no longer valid. If you see this ensure you have copied the entire key including the entire key with line breaks

Example:

```
-----BEGIN PRIVATE KEY----- 
some uber long varchar set is here
-----END PRIVATE KEY----- 
```

<figure><img src="../../.gitbook/assets/400-bad-jwt.png" alt=""><figcaption><p>400 invalid_token</p></figcaption></figure>





![Graphical user interface, text, application, email

Description automatically generated](<../../.gitbook/assets/16 (3).png>)

**Invalid IMS\_ORG**

<figure><img src="../../.gitbook/assets/invalid IMS ORG.png" alt=""><figcaption></figcaption></figure>

*
