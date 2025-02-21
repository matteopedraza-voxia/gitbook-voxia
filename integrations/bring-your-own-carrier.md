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

# Bring Your Own Carrier

{% hint style="info" %}
Voxia supports incoming and outgoing calls. Your SIP provider may need our IP address, `35.245.182.192`, to ensure connectivity.
{% endhint %}

To integrate your own SIP carrier with Voxia, follow the steps below:

### Step 1: Access SIP Integration

* Go to the _**Integrations**_ tab on your Voxia dashboard.
* Click on the `Connect` in the SIP Integration option to begin setting up your carrier.



<figure><img src="../.gitbook/assets/New SIP.png" alt=""><figcaption></figcaption></figure>

### Step 2: Add SIP Details

* **SIP Name**: Enter a unique name for your SIP connection.
* **E.164 syntax:** Numbers are formatted \[+] \[number including country and area code].
* **Outbound authentication:** Enable if authentication is required.
  * **Username**: Enter the username provided by your SIP provider.
  * **Password**: Enter the password associated with your SIP account.
* **Tech prefix:** Enable if tech prefix is required.
* **SIP Diversion Header:** Enable for authenticated outgoing call.
* **URL**: Provide the URL given by your SIP provider.
* **Port**: The default is 5060.
*   **Add SIP Gateway:** Configure same phone number for both incoming and outgoing calls.

    * For Telnyx set up, configure the regions IPs according to the [SIP Regions for Telnyx documentation](https://sip.telnyx.com/).



    <figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

Click `Next` to proceed.

### Step 3: Configure Phone Numbers

After clicking `Next`, you will be prompted to enter the phone numbers associated with your SIP in the next window.

{% hint style="success" %}
Alternatively, you can go to the `Phone numbers` tab and click on `Add SIP Numbers` to manually add phone numbers at any time.
{% endhint %}
