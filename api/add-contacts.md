---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Add Contacts

{% hint style="warning" %}
The API call adds the updated contact to the specified campaign in Voxia. If the phone number is already present on this campaign, it will update the name and other fields based on the latest invocation.
{% endhint %}

{% openapi src="../.gitbook/assets/openapi (2).json" path="/campaigns/{campaignId}/contacts" method="post" %}
[openapi (2).json](<../.gitbook/assets/openapi (2).json>)
{% endopenapi %}



{% hint style="info" %}
To check how to set the API Key credentials, go to the [Authorization ](authorization.md)tab.
{% endhint %}
