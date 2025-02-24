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

# Uploading Contacts

### Adding Contacts Manually

* **Navigate to Your Campaign**: From the main dashboard, click on the campaign you want to add contacts to.
* **Add Contacts**: Click on the "Add Contacts" button located on the top right of the campaign page. In the window that opens, click on the "Add Manually" tab at the top.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 12.35.18.png" alt=""><figcaption></figcaption></figure>

* **Enter Contact Details**: Start filling in the contact details as required by the variables included in the campaign, such as name, phone number, email address, and any custom fields.
* **Finalize Import**: After entering all the necessary details, review the information to ensure accuracy. Click on 'Finalize import' located on the top right of the window.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 15.29.20.png" alt=""><figcaption><p>Manually enter contacts, press Finalize Import when done.</p></figcaption></figure>

* **Wait for Processing**: Wait for the platform to complete the processing of the data. This may take some time depending on the volume of contacts being added.
* **View Summary**: Once the import is finalized, a summary will be displayed showing the number of contacts successfully added and the number of contacts that were not added.&#x20;
* **Complete the Process:** Click on the 'Finalize import' button located on the top right of the window again to confirm the completion of the process.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 15.31.51.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Duplicate Handling**: Note that contacts with phone numbers that are already included in the campaign will not be uploaded again to avoid duplicates.
{% endhint %}

### Uploading Contacts via CSV

{% hint style="info" %}
#### CSV Format

* **Header Format:** Ensure your column headers follow a consistent style that matches the variable names used in your campaign. For 'Property Address', acceptable formats include 'PropertyAddress', 'propertyAddress', 'Property Address', 'Property\_address', and 'property address'.&#x20;
  * For the name of the contact, use 'name' or 'Name'.&#x20;
  * The phone number must always be written as 'phone number' in various acceptable formats, as seen above.
  * For the email, use 'email' or 'Email'.
* **Include Country Code**: Make sure that phone numbers include the country code to ensure they are recognized correctly.
* **Spaces and Symbols**: It's acceptable for phone numbers to contain spaces and symbols like dashes or parentheses. These characters will not interfere with the upload process, so feel free to include them if they are a part of your phone number formatting in the dataset.

{% code title="CSV Format Example.csv" fullWidth="false" %}
```csv
name,phoneNumber,propertyAddress,email
John,+1 555 555 1234,123 Maple Street,john@voxia.ai
Tom,+1 555 555 5678,456 Maple Street,tom@voxia.ai
```
{% endcode %}
{% endhint %}

* **Navigate to Your Campaign:** From the main dashboard, click on the campaign you want to add contacts to.
* **Add Contacts**: Click on the "Add Contacts" button located on the top right of the campaign page. In the window that opens, click on the "Select file" button to browse and choose the CSV file from your computer.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 15.33.10.png" alt=""><figcaption><p>Upload contacts with a CSV file.</p></figcaption></figure>

* **Finalize Import**: After you have filled in the contacts via CSV, click on the 'Finalize import' button located on the top right of the window.
* **Wait for Processing**: Wait for the platform to complete the processing of the data. This may take some time depending on the volume of contacts being imported.
* **View Summary**: Once the import is finalized, a summary will be displayed showing the number of contacts successfully added and the number of contacts that were not added.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 15.46.54.png" alt=""><figcaption></figcaption></figure>

* **Complete the Process:** Click on the 'Finalize import' button located on the top right of the window again to confirm the completion of the process.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-14 at 15.44.37.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Duplicate Handling**: Note that contacts with phone numbers that are already included in the campaign will not be uploaded again to avoid duplicates.
{% endhint %}
