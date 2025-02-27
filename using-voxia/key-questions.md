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

# Key Questions

By adding Key Questions to your script steps, you create a handy reference for quick analysis and data retrieval. This section takes place under the campaign summary:

<figure><img src="../.gitbook/assets/Screenshot 2025-02-26 at 09.31.17.png" alt=""><figcaption><p>Key questions will be listed in the Post-call section.</p></figcaption></figure>

### Summary and Post-Processing

In this section you will be able to set the Interest Criteria (conditions under which a call can be considered **Interested**) and the Key Questions.

There are two types of Key Questions:

* **Step keys:** the analysis will be made related to a specific step or question.
* **Global keys:** the analysis will be made along the whole conversation.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Adding Key Questions

#### Step Key Questions

* Navigate to the script where you want to add the Key Questions.
* Find the step number located on the left side of the step you want to summarize.
* Click on the step number. This action will open a window to set the Key for the step.

<figure><img src="broken-reference" alt=""><figcaption><p>Press the star icon left to the step to create your Key Question.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 18.05.46.png" alt=""><figcaption><p>Press the star icon to set a step as key question.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 18.07.17.png" alt=""><figcaption></figcaption></figure>

* Title, Description and Key Type will be automatically created for your Key Question according to the step description. This is data that can be changed.
* There are several types of question to select according to the desired output needed:
  * Open question
  * Single choice
  * Multiple choice
  * Yes/No
  * Number
  * Date
  * Time

{% hint style="info" %}
You can add multiple titles to each step by repeating the above process, generating multiple outputs for the summary.
{% endhint %}

#### Global Key Questions

* Navigate to the summary window into the Post-Call Analysis.
* Click on the "+ Add" button to create a new Key Question.
* Complete the required fields:
  * **Title:** Displayed in the summary.
  * **Description:** Instruction to the AI on what information to extract.
  * **Key Type:** Desired output response.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

> #### Removing Key Question Titles
>
> To delete a title, hover over the title and click on the remove icon that appears on the right side of it.

### Key Questions in Summaries

* Once added, these titles will be displayed in the 'Interested' contact summary section.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-17 at 17.06.19 copy.png" alt=""><figcaption></figcaption></figure>

* For Webhooks, the summary will be structured as follows:

```json
"summary": {
    "Contact willingness": {
      "description": "Tell if the contact was willing to tell personal information",
      "options": [],
      "order": 3,
      "type": "YES_NO",
      "value": true
    },
    "Residency Inquiry": {
      "description": "Provide a yes or no response indicating whether you reside in the specified country.",
      "options": [],
      "order": 2,
      "type": "YES_NO",
      "value": true
    },
    "Schedule Call": {
      "description": "Extract the preferred day and time for the follow-up call.",
      "options": [],
      "order": 1,
      "type": "OPEN_QUESTION",
      "value": "today at five pm"
    }
  }
```
