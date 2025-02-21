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

# Webhook Overview

{% hint style="info" %}
To receive information after the call, add a Webhook URL.
{% endhint %}

### Configure a Webhook

1. Navigate to the Settings of the specific campaign you want to configure.
2. Scroll to the bottom of the settings window.
3. Click on 'Add Webhook URL'.
4. Enter the URL where you want the Webhook data to be sent.
5. Select the call statuses where on which the webhook will be triggered.
6. Click on 'Save changes' located at the top right of the window

#### Possible Event triggers

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

### Webhook Response Example

{% code fullWidth="false" %}
```json
{
  "callStatus": "COMPLETED",
  "createdAt": "2024-03-11T14:56:41.642Z",
  "phoneFrom": "+15555551234",
  "status": "INTERESTED",
  "postProcessStatus": "INTERESTED",
  "hangUpReason": "CALL_FINISHED",
  "duration": 128,
  "totalDuration": 150,
  "contactStatus": {
    "callMeLater": false,
    "doNotCall": false,
    "wrongNumber": false
  },
  "conversationFlow": [
    ],
  "summary": {
    "Inquiry Asked": {
      "description": "Interested in learning more about our services",
      "options": [
      ],
      "order": new NumberInt("1"),
      "type": "YES_NO",
      "value": false
    }
  },
  "campaign": {
    "id": "{campaignId}",
    "name": "{campaignName}"
  },
  "id": "{callId}",
  "contact": {
    "id": "{contactId}",
    "name": "John",
    "phoneNumber": "+1234567890",
    "data": {
      "email": "john@voxia.ai",
      "position": "Product Manager",
      "company": "Voxia"
    }
  },
  "twilio": {
    "accountSid": "{accountSid}",
    "callSessionId": "{callSessionId}"
  },
  "organizationId": "{organizationId}",
  "transcript": [
    {
      "content": "Hello, this is Voxia. How can I assist you today?",
      "role": "Voxia"
    },
    {
      "content": "Hi, can you tell me more about your services?",
      "role": "user"
    },
    {
      "content": "Certainly! We offer personalized AI calling services. Would you like to schedule a demo?",
      "role": "Voxia"
    },
    {
      "content": "Yes, that sounds great. Thank you!",
      "role": "user"
    },
    {
      "content": "You're welcome! I'll set that up and send you a confirmation. Have a great day!",
      "role": "Voxia"
    }
  ],
  "interested": {
    "description": "The caller showed interest in scheduling a demo, indicating a positive engagement.",
    "reached": true
  },
  "events": [
    {
      "type": "SMS",
      "data": {
        "sent": true,
        "status": "queued",
        "sentAt": "2024-11-28T22:37:01.000Z",
        "sentTo": "+1999999999",
        "uri": "{uri}",
        "smsSid": "{smsSid}",
        "sentFrom": "+1999999999",
        "text": "{smsTemplateText}"
      }
    },
    {
      "type": "FORWARD",
      "data": {
        "phoneNumber": "+1999999999",
        "contactAsCallerId": true
      }
    }
  ],
  "webhookUrl": "{webhookUrl}",
  "webhookEvent": "CONNECTED",
  "webhookEvents": [
        "HANG_UP",
        "CONNECTED",
        "POST_PROCESSING_FINISHED:NOT_INTERESTED",
        "POST_PROCESSING_FINISHED:CALL_ME_LATER",
        "POST_PROCESSING_FINISHED:INTERESTED",
        "POST_PROCESSING_FINISHED:VOICE_MAIL"
    ],
    "webhookStatuses": [
        "INTERESTED",
        "NOT_INTERESTED",
        "CALL_ME_LATER",
        "WRONG_NUMBER",
        "DO_NOT_CALL",
        "COMPLETED",
        "FAILED",
        "VOICE_MAIL",
        "BUSY",
        "NO_ANSWER"
    ],
  "isTestCall": false,
  "sessionId": "{sessionId}",
  "slackUrl": "{salckUrl}"
}
```
{% endcode %}

### Webhook Fields Description

<table><thead><tr><th width="191">Field</th><th>Description</th></tr></thead><tbody><tr><td><code>createdAt</code></td><td>Timestamp when the call was initiated in ISO 8601 format.</td></tr><tr><td><code>phoneFrom</code></td><td>Phone number from which the call originated.</td></tr><tr><td><code>status</code></td><td><p>Composite status of a call. It includes the call status, the reason for call hang up, and the candidate status. </p><p></p><p><strong>Call progress status:</strong></p><ul><li><code>NEW</code></li><li><code>IN_PROGRESS</code></li><li><code>BUSY</code></li><li><code>NO_ANSWER</code></li><li><code>VOICE_MAIL</code></li><li><code>FAILED</code></li></ul><p><strong>Call connection status:</strong></p><ul><li><code>USER_REQUESTED_HANGUP</code></li><li><code>ADMIN_MANUAL_HANGUP</code></li><li><code>VOICE_MAIL_DETECTED</code></li><li><code>SILENCE_DETECTED</code></li><li><code>USER_MANUAL_HANGUP</code></li><li><code>CONVERSATION_LLM_TECHNICAL_ISSUES</code></li><li><code>OTHER_TECHNICAL_ISSUES</code></li><li><code>CALL_FINISHED</code></li><li><code>CALL_FORWARDED</code></li><li><code>UNKNOWN</code></li><li><code>SOCKET_DISCONNECTED</code></li></ul><p><strong>Contact response to call:</strong></p><ul><li><code>INTERESTED</code>: The contact expressed interest in the purpose of the call.</li><li><code>NOT_INTERESTED</code>: The contact is not interested in the purpose of the call.</li><li><code>CALL_ME_LATER</code>: The contact requested a follow-up call at a later time.</li><li><code>PENDING</code>: The contact has been returned to the call queue for further attempts.</li><li><code>WRONG_NUMBER</code>: The number dialed did not correspond to the intended contact.</li><li><code>DO_NOT_CALL</code>: The contact requested not to receive future calls.</li></ul><p></p></td></tr><tr><td><code>callStatus</code></td><td><p>Call status:</p><ul><li><code>NEW</code></li><li><code>IN_PROGRESS</code></li><li><code>FAILED</code></li><li><code>COMPLETED</code>: The user answered and the call ended successfully.</li><li><code>NO_ANSWER</code></li><li><code>BUSY</code></li><li><code>VOICE_MAIL</code></li><li><code>DO_NOT_CALL_REGISTRY_MATCHED</code></li></ul></td></tr><tr><td><code>postProcessStatus</code></td><td><p>Candidate status for that call:</p><ul><li><code>INTERESTED</code> </li><li><code>NOT_INTERESTED</code></li><li><code>CALL_ME_LATER</code></li><li><code>WRONG_NUMBER</code></li><li><code>DO_NOT_CALL</code></li></ul></td></tr><tr><td><code>events</code></td><td><p>Details about specific call events:</p><ul><li><p><code>SMS</code></p><ul><li>Data regarding origin, destination and content</li></ul></li><li><code>FORWARDED CALL</code></li><li><p><code>MEETING</code></p><ul><li>Data regarding slot booked, date sent and destination email.</li></ul></li></ul></td></tr><tr><td><code>webhookUrl</code></td><td>URL to which the Webhook data is sent post-call.</td></tr><tr><td><code>webhookEvent</code></td><td><p>Event related to the<a href="webhook-overview.md#possible-event-triggers"> webhook trigger</a>:</p><ul><li><code>DIALING</code></li><li><code>CONNECTED</code></li><li><code>FAILED</code></li><li><code>COULD_NOT_CONNECT:BUSY</code></li><li><code>COULD_NOT_CONNECT:NO_ANSWER</code></li><li><code>FORWARDED</code></li><li><code>HANG_UP</code></li><li><code>POST_PROCESSING_FINISHED:VOICE_MAIL</code></li><li><code>POST_PROCESSING_FINISHED:INTERESTED</code></li><li><code>POST_PROCESSING_FINISHED:NOT_INTERESTED</code></li><li><code>POST_PROCESSING_FINISHED:WRONG_NUMBER</code></li><li><code>POST_PROCESSING_FINISHED:CALL_ME_LATER</code></li><li><code>POST_PROCESSING_FINISHED:DO_NOT_CALL</code></li><li><code>FORWARDED_CALL_FINISHED</code></li></ul></td></tr><tr><td><code>webhookEvents</code></td><td><a href="webhook-overview.md#possible-event-triggers">List of selected events </a>for triggering the webhook.</td></tr><tr><td><code>hangUpReason</code></td><td><p>Reason for the call termination:</p><ul><li><code>USER_REQUESTED_HANGUP</code>: User asked to hang up.</li></ul><ul><li><code>ADMIN_MANUAL_HANGUP</code>: Call ended by an admin.</li></ul><ul><li><code>USER_MANUAL_HANGUP</code>: User manually ended the call.</li></ul><ul><li><code>CALL_FINISHED</code>: Call ended after the completion of all interactions.</li><li><code>CALL_FORWARDED</code>: Call transferred to a designated phone number.</li></ul></td></tr><tr><td><code>duration</code></td><td>Duration of the call with Voxia's agent in seconds.</td></tr><tr><td><code>totalDuration</code></td><td>Total duration of the call including the forwarded call duration in seconds.</td></tr><tr><td><code>contactStatus</code></td><td><p>Object indicating the contact's preferences:</p><ul><li><code>callMeLater</code>: Boolean indicating if the contact requested a callback later.</li></ul><ul><li><code>doNotCall</code>: Boolean indicating if the contact requested not to be called again.</li></ul><ul><li><code>wrongNumber</code>: Boolean indicating if the contact reported this as a wrong number.</li></ul></td></tr><tr><td><code>summary</code></td><td>Object summarizing the <a href="../using-voxia/key-questions.md">Key Questions</a> made during the call.</td></tr><tr><td><code>campaign</code></td><td><p>Information about the campaign associated with the call:</p><ul><li><code>id</code>: Campaign id.</li></ul><ul><li><code>name</code>: Name of the campaign.</li></ul></td></tr><tr><td><code>id</code></td><td>Unique identifier for the call.</td></tr><tr><td><code>contact</code></td><td><p>Details about the person contacted:</p><ul><li><code>id</code>: Contact's identifier.</li><li><code>name</code>: Contact's name.</li></ul><ul><li><code>phoneNumber</code>: Contact's phone number.</li></ul><ul><li><code>data</code>: Contains additional properties that can be used as variables in the script during the call</li></ul></td></tr><tr><td><code>twilio</code></td><td><p>Twilio information:</p><ul><li><code>accountSid</code>: Unique identifier for the Twilio account.</li></ul><ul><li><code>callSessionId</code>: Unique session identifier for the call.</li></ul></td></tr><tr><td><code>organizationId</code></td><td>Unique identifier for the organization.</td></tr><tr><td><code>transcript</code></td><td>Array of dialogue exchanges during the call, with each entry detailing the content spoken and the role of the speaker.</td></tr><tr><td><code>interested</code></td><td><p>Object detailing whether the caller expressed interest in the services:</p><ul><li><code>description</code>: The Interest Criteria defined by the user for the campaign.</li></ul><ul><li><code>reached</code>: Boolean indicating whether the Interest Criteria was reached.</li></ul></td></tr><tr><td><code>isTestCall</code></td><td>Boolean indicating if the call was a test call.</td></tr><tr><td><code>slackUrl</code></td><td>Webhook Url if the account is integrated with Slack</td></tr></tbody></table>
