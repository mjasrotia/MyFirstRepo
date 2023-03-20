# Overview

![](<.gitbook/assets/0 (3).jpeg>)

### **Lab Overview**

Being able to work with the Experience Platform APIs is critical to being able to understand how to automate and operationalize various features of the platform. Defining schemas and understanding how data is described by those schemas is one of the first things a customer will do on Adobe Experience Platform as they define their data architecture.

This lab will introduce you to the Adobe Experience Platform schema design experience utilizing only the API’s. You will learn how to create your own schemas utilizing existing XDM components, adding your own customizations in XDM and identifying and creating various identity descriptors for use with the Real-Time Customer Profile.

### **Learning Objectives**

What should you walk away with after taking this Lab?

Be able to build a schema utilizing only the Experience Platform API’s through a variety of XDM foundational components such as:

*
  1. Classes
  2. Field Group’s
  3. Descriptors
     1. Identities (including Primary)
     2. Relationship
     3. Reference

### **Reference Material**

Refer this Source to XDM mapping sheet which you would have finalized before creating the schemas.\


| Source Column      | XDM Property                 | XDM Descriptor | XDM Field Group/Class          |
| ------------------ | ---------------------------- | -------------- | ------------------------------ |
| customerID         | \_devbc.customerID           | PI             | Customer Account Details       |
| firstName          | person.name.firstName        |                | Demographic Details            |
| lastName           | person.name.lastName         |                | Demographic Details            |
| email              | personalEmail.address        | I              | Personal Contact Details       |
| mobilePhone        | mobilePhone.number           |                | Personal Contact Details       |
| birthDate          | person.birthDayAndMonth      |                | Demographic Details            |
| birthDate          | person.birthYear             |                | Demographic Details            |
| billingstreet      | billingAddress.street1       |                | Personal Contact Details       |
| billingcity        | billingAddress.city          |                | Personal Contact Details       |
| billingstate       | billingAddress.state         |                | Personal Contact Details       |
| billingpostalCode  | billingAddress.postalCode    |                | Personal Contact Details       |
| shippingstreet     | shippingAddress.street1      |                | Personal Contact Details       |
| shippingcity       | shippingAddress.city         |                | Personal Contact Details       |
| shippingstate      | shippingAddress.state        |                | Personal Contact Details       |
| shippingpostalCode | shippingAddress.postalCode   |                | Personal Contact Details       |
| emailOptIn         | consents.marketing.email.val |                | Consent And Preference Details |
| smsOptIn           | consents.marketing.sms.val   |                | Consent And Preference Details |
| accountCreateDate  | \_devbc.account.createDate   |                | Customer Account Details       |
| accountEndDate     | \_devbc.account.endDate      |                | Customer Account Details       |
| createDate         | repo.createDate              |                | XDM Individual Profile         |
| modifyDate         | repo.modifyDate              |                | XDM Individual Profile         |
| source             | \_devbc.account.acqSource    |                | Customer Account Details       |
| planID             | \_devbc.plan\_planID         | RI             | Customer Account Details       |
| planName           | \_devbc.plan.name            |                | Customer Account Details       |

### **Glossary**

| Term                                                                         | Description/Definition                                        |
| ---------------------------------------------------------------------------- | ------------------------------------------------------------- |
| \_devbc                                                                      | Sample tenant namespace                                       |
| https://platform.adobe.io/data/foundation/ schemaregistry/tenant             | Schema Registry end point to access tenant XDM components     |
| https://platform.adobe.io/data/foundation/ schemaregistry/global             | Schema Registry end point to access tenant XDM components     |
| https://platform.adobe.io/data/foundation/ schemaregistry/global/schemas     | Schema Registry end point for standard XDM Schemas            |
| https://platform.adobe.io/data/foundation/ schemaregistry/tenant/schemas     | Schema Registry end point for tenant XDM Schemas              |
| https://platform.adobe.io/data/foundation/ schemaregistry/global/mixins      | Schema Registry end point for standard XDM Field Groups       |
| https://platform.adobe.io/data/foundation/ schemaregistry/tenant/schemas     | Schema Registry end point for tenant XDM Field Groups         |
| https://platform.adobe.io/data/foundation/ schemaregistry/global/descriptors | Schema Registry end point for standard XDM Schema Descriptors |
| https://platform.adobe.io/data/foundation/ schemaregistry/tenant/descriptors | Schema Registry end point for tenant XDM Schema Descriptors   |
| **GET**                                                                      | API call to fetch an XDM component                            |
| **POST**                                                                     | API call to create an XDM component                           |
| **PATCH**                                                                    | API call to update or add to an existing XDM component        |
