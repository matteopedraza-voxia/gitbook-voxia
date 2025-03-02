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

# Validating Webhook Signatures

When integrating with Voxia, it's important to ensure that the webhook payloads you receive are indeed from Voxia. To facilitate this, Voxia signs each payload with a private key.&#x20;

Your system can verify these payloads using the corresponding public key, which Voxia provides. This process guarantees the integrity and authenticity of the data sent to your system.

### **Overview of the Process**

#### **Signed Webhooks**

Each webhook sent by Voxia is securely signed using a cryptographic process. Voxia utilizes HMAC (Hash-based Message Authentication Code) with the SHA-256 algorithm for signing. The procedure involves using both the webhook payload and a unique encryption key as inputs to generate a signature. This method ensures that the signature is tightly bound to the payload and the encryption key, making it both unique and secure.

The resulting signature is then attached to the webhook request within a custom header named `X-Voxia-Signature`. This setup enables the recipient to readily extract and validate the signature against the expected payload, ensuring its authenticity.

#### **Verification Process**

Upon receiving a webhook, follow these steps to verify its authenticity:

{% hint style="warning" %}
For whitelabel, you’ll receive the signature as `X-Signature` instead of `X-Voxia-Signature`.
{% endhint %}

1. Extract both the payload and the `X-Voxia-Signature` header from the incoming request.
2. Use the public key to verify the signature instead of computing the HMAC yourself. In this case, the public key would be used to check that the `X-Voxia-Signature` matches a valid cryptographic signature for the received payload.
3. Compare the result:
   * If the public key verification succeeds, then the payload is confirmed as authentic.
   * If the verification fails, the payload should be considered compromised or originating from an untrusted source and discarded.

### Public Key

Ensure that your public key file is loaded into your application as shown in the examples above. Here is a template for how your public key might appear:

{% code title="public-key.pem" %}
```
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAqlIbBLMO6BYo8qiVke3o
oGnKikX1n+htu/TQN6IaPF81+4puf6wdSf4aQkh+PkbWeVExsazpoKr/EOWAXsGy
DxYuoROtRhfo/nskQDjfk78DZRWkj7RW7lMLe+MilUaMPQnDQtDAIc9d/9yoGGjt
GRHmfgfswt6f+zOyqqbOzoGD5kDdw8d5ZBiwNGFv1BFkDN5Ivj5fsMrGc3nFpaHI
kSC8beE0NQdDbN9k4GV9C6OOEoDJvZiQwg3Ck3hTO44mOXj+yQKdPm7bdShd4Ap6
wgfVDVU4LvvRLEn1fW0n58f7nBA5f9SNpE6NTipjg0qWIcilZtL/Lj90XroHCqZi
7QIDAQAB
-----END PUBLIC KEY-----
```
{% endcode %}

### Validating Signature Examples

Below are detailed examples for validating the webhook payload using the public key in both JavaScript and Python.

#### **JavaScript**

{% code overflow="wrap" %}
```javascript
const crypto = require('crypto');
const fs = require('fs');

// Load the public key (Ensure this key is securely stored and only accessible to your application)
const publicKey = fs.readFileSync('path/to/public-key.pem', 'utf8');

/**
 * Validate webhook payload signature using RSA public key.
 * @param {Object} payload - The webhook payload
 * @param {string} receivedSignature - The signature from 'X-Voxia-Signature' header, encoded in base64
 * @returns {boolean} - Returns true if the signature is valid
 */
function validateWebhookPayload(payload, receivedSignature) {
  const payloadString = JSON.stringify(payload);
  
  const verify = crypto.createVerify('RSA-SHA256');
  verify.update(payloadString);
  verify.end();
  
  return verify.verify(publicKey, receivedSignature, 'base64');
}

// Example usage
const receivedPayload = { event: 'call_finished', callId: '12345', status: 'completed' };
const receivedSignature = 'base64-encoded-signature-from-header';

const isValid = validateWebhookPayload(receivedPayload, receivedSignature);

console.log(isValid ? 'Valid Signature' : 'Invalid Signature');
```
{% endcode %}

#### Python

```python
import json
import hmac
from Crypto.Signature import pkcs1_15
from Crypto.Hash import SHA256
from Crypto.PublicKey import RSA
from base64 import b64decode

def validate_webhook_payload(payload: dict, received_signature: str) -> bool:
    """
    Validate webhook payload signature using RSA public key.
    
    :param payload: The webhook payload (dictionary)
    :param received_signature: The signature from 'X-Voxia-Signature' header, encoded in base64
    :return: True if the signatures match, False otherwise
    """
    payload_string = json.dumps(payload)
    hash_payload = SHA256.new(payload_string.encode('utf-8'))
    
    # Load the public key (Ensure this key is securely stored and only accessible to your application)
    with open('path/to/public-key.pem', 'r') as f:
        public_key = RSA.import_key(f.read())
        print('public_key: ',public_key)
        try:
            pkcs1_15.new(public_key).verify(hash_payload, b64decode(received_signature))
            return True
        except (ValueError, TypeError):
            return False

# Example usage
received_payload ={'event': 'call_finished', 'callId': '12345', 'status': 'completed'}

received_signature = 'base64-encoded-signature-from-header'

is_valid = validate_webhook_payload(received_payload, received_signature)
print(is_valid)
print("Valid Signature" if is_valid else "Invalid Signature")

```



{% hint style="info" %}
By implementing these steps, you can securely verify that the webhook payloads you process are genuine, ensuring reliable and secure operation of your integrations with Voxia. This validation process is essential for maintaining the integrity of communications between Voxia and your system.
{% endhint %}
