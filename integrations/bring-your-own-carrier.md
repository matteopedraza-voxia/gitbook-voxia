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
Voxia supports incoming and outgoing calls. Your SIP provider may need our IP address: `35.245.182.192`, to ensure connectivity.
{% endhint %}

To integrate your own SIP carrier with Voxia, follow the steps below:

### Step 1: Access SIP Integration

* Go to the _**Integrations**_ tab on your Voxia dashboard.
* Click on the `Connect` in the SIP Integration option to begin setting up your carrier.



<figure><img src="../.gitbook/assets/New SIP.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-02-18 at 09.38.23.png" alt=""><figcaption><p>Setup a SIP under Integrations.</p></figcaption></figure>

## Step 2: Add SIP Details

* **SIP Name**: Enter a unique name for your SIP connection.
* **E.164 syntax:** Numbers are formatted \[+] \[number including country and area code].
* **Outbound authentication:** Enable if authentication is required.
  * **Username**: Enter the username provided by your SIP provider.
  * **Password**: Enter the password associated with your SIP account.
* **Tech prefix:** Enable if tech prefix is required.
* **SIP Diversion Header:** Enable for authenticated outgoing call.
* **URL**: Provide the URL given by your SIP provider.
* **Port**: The default is 5060.
* **Add SIP Gateway:** Configure same phone number for both incoming and outgoing calls.
  * For Telnyx set up, configure the regions IPs according to the [SIP Regions for Telnyx documentation](https://sip.telnyx.com/).

<figure><img src="../.gitbook/assets/Screenshot 2025-02-18 at 09.32.02 (2).png" alt=""><figcaption><p>Configure your SIP.</p></figcaption></figure>

Click `Next` to proceed.

## Step 3: Configure Phone Numbers

After clicking `Next`, you will be prompted to enter the phone numbers associated with your SIP in the next window.

{% hint style="success" %}
Alternatively, you can go to the `Phone numbers` tab and click on `Add SIP Numbers` to manually add phone numbers at any time.
{% endhint %}

## Setup Multiple SIPs

* Go to the _**Integrations**_ tab on your Voxia dashboard.
* Click on the `Connect` in the SIP Integration option to setup an additional carrier.
* Add your SIP details.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-20 at 13.40.37.png" alt=""><figcaption><p>Look for an unconnected SIP slot.</p></figcaption></figure>



## Add Telnyx Phone Numbers

Guide regarding your Telnyx account, purchasing phone numbers, retrieving your SID configuration, and using these data in Voxia’s app.

### Step 1: Buy a Telnyx phone number

* Go to the _**Numbers**_ tab on your Telnyx sidebar.
* If you don't already have a phone number, click on the `Buy number` to get a phone number in Telnyx.

<figure><img src="../.gitbook/assets/Telnyx1 (2).png" alt=""><figcaption></figcaption></figure>

### Step 2: Create a SIP connection

* Go to the **Voice** tab and select **SIP Trunking** to create a SIP Connection.
* Click on the **Create SIP Connection** button to add a new connection.
* Select a Name and **IP Address** as the connection Type.
* In the **Authentication & Routing Configuration** section add Voxia's public IP and the default port **5060.**

{% hint style="info" %}
Voxia's public IP address is `35.245.182.192`
{% endhint %}

<figure><img src="../.gitbook/assets/Telnyx2 (2).png" alt=""><figcaption></figcaption></figure>

Go to _**Inbound**_ to continue the settings.

* According to the campaign region, set the SIP Region according to [Telnyx documentation](https://sip.telnyx.com/).

### Step 3: Configure Phone Numbers

Click on the `Numbers` tab to select the acquired telephone number that will be used for the inbound campaign.

{% hint style="info" %}
To set up the Telnyx number in Voxia, go to the [BYOC documentation](bring-your-own-carrier.md).
{% endhint %}
