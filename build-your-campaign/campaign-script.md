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

# Campaign Script

This guide provides an overview of how to create a versatile and effective campaign script within the Voxia platform.&#x20;

Tailor the conversation flow to meet the unique needs of your campaign, whether it's for inbound or outbound calls.

### Understanding the Script Creation Process

Creating a campaign script involves setting up a series of decision points and responses that guide the conversation with your clients.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>Example Flowchart for a 'Speed to Lead' Campaign of Voxia</p></figcaption></figure>

### Steps to Create Your Script

#### **Initiate with the Intro Script**

* **Inbound Calls**: As a suggestion, you might begin your script with an introductory script node where you confirm the client's identity by asking for their name and inquiring about their well-being. However, feel free to adjust this approach based on your specific needs.
* **Outbound Calls**: As a suggestion, start by confirming the client’s identity and then proceed with the planned interaction. This is just a guideline, and you can tailor it as required.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

#### **Branching the Conversation**

*   After the initial engagement, introduce a question to guide the conversation. Based on the client's response, you can expand the script:

    * Click the `+` button next to the current node.
    * Select `Add Subflow` to create a new branch.
    * In the new node, label it with a title that represents the client’s latest response which guides the agent to this node. Alternatively, you can simply give a title to this node based on its content.



    <figure><img src="../.gitbook/assets/image (19).png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="info" %}
**Note**: If no decision split is required, you can continue the script in the same node.
{% endhint %}

#### **Customize Node Content**

* Customize the dialogue and the questions in each node according to the campaign goals. Refer to the [Customize Steps](customizing-steps.md) page for more details.

{% hint style="warning" %}
**Note**: Each node must contain at least one step.
{% endhint %}

#### **Directing Flow Between Nodes**

* To lead the script from a subflow back to a specific node or to continue the script from a particular point:
  * Click the `+` button next to the node from which you want to continue.
  * Select `Go to Block`.
  * Choose the destination node. Optionally, you can set a title to specify if the script should lead to this node based on client’s latest response.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Note:** You can add as many subflows as needed to accommodate various branches of the conversation.
{% endhint %}

#### **Generating Interest Criteria**

After completing the script, click the `Generate Interest Criteria` button located in the top left corner to define the conditions under which a call can be considered **Interested**.

<figure><img src="../.gitbook/assets/image (37).png" alt="" width="375"><figcaption></figcaption></figure>

#### **Validate the Flow**

* Ensure all node links are correctly made to prevent any dead ends or loops in the conversation.
* Preview and test the campaign. Conduct test calls to check the flow and make necessary adjustments.
