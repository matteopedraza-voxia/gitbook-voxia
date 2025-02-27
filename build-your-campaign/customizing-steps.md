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

# Customizing Steps

This guide provides detailed instructions on how to personalize the dialogue and questions in each node of your campaign script within the Voxia platform.

* **Add Call Steps**: Click the `New Step` button to begin adding steps that the assistant will follow during the call.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-17 at 17.48.57.png" alt=""><figcaption><p>Adding a call step.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption><p>Call step added.</p></figcaption></figure>

* **Schedule Meetings**:
  * Press the `Schedule a Meeting` button.
  * For scheduling, connect to Cal.com through the integrations tab.
  * Before offering time slots from your account, decide on the content for the assistant to say.
  * Choose the relevant event from the dropdown.
  * Define how many days in advance clients can schedule meetings by setting the _Schedule days ahead_ field. We recommend not to use more than 14 days in advance.
  * For scenarios when no time slots are available, configure how the assistant should react:
    * **Avoid Calling**: Select this option to prevent the assistant from making calls when no slots are available.
    * **Use Fallback Phrase**: Choose this option to have the assistant use a fallback phrase. Upon selection, a text field will open where you can insert the specific sentence the assistant should say.

<figure><img src="../.gitbook/assets/Screenshot 2024-08-16 at 19.23.14 (1).png" alt=""><figcaption><p>Scheduling a meeting from a step.</p></figcaption></figure>

{% hint style="warning" %}
Note that to add this step, you need to have an **`Email`** for each contact.
{% endhint %}

* **Call Forwarding**:
  * Press the `Call Transfer` button.
  * Enter a _Call Transfer Phrase_ in the provided text field. This phrase will be spoken by the assistant before the call is transferred.
  * Specify the phone number to which the call will be transferred. **Ensure to include the country code.**
  * Choose whether the Caller ID for the forwarded call will be the campaign's number or the contact's number.



<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>Forwarding a call with a step.</p></figcaption></figure>

*   **Setup SMS**:&#x20;

    * Press the `SMS` button.
    * Add a phrase for the assistant to say before sending an SMS and set the content of the SMS in the SMS Template.



<figure><img src="../.gitbook/assets/Screenshot 2025-02-17 at 18.23.47.png" alt=""><figcaption><p>Setting up an SMS within a step.</p></figcaption></figure>

**Editing Steps**

* **Reorder Steps**: Long press and drag a step number to change the order.
* **Step Options**: To manage the content of a step, click the buttons on the right. You can:
  * **Play**: Hear how the sentence will be said.
  * **Rephrase**: Generate a new version of the sentence.
  * **Delete Step**: Remove the step from the script.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-17 at 18.26.14.png" alt=""><figcaption><p>You can play, rephrase and Delete each step.</p></figcaption></figure>

#### **Call Script Variables**

* **Add Variables**: Click the  `+`  icon under each step to open the variable entry window.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-17 at 17.55.01.png" alt=""><figcaption><p>Adding variables to a step.</p></figcaption></figure>

* **Enter and Save Variables**: In the window that opens, type in the variables you need and press enter after each one to confirm. Once you have finished adding all the variables, click the `Save` button to apply the changes.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-17 at 18.02.50.png" alt=""><figcaption><p>Creating a new variable on a step.</p></figcaption></figure>

{% hint style="info" %}
Variables need to be added through uploading contacts. See [API documentation](../api/add-contacts.md) and [uploading contacts](../using-voxia/uploading-contacts.md) pages for more details.
{% endhint %}
