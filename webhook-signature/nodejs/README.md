
# Verify Payiano Webhook Signature

This project provides a JavaScript example for verifying webhook signatures sent by the Payiano API using `HMAC-SHA256`.

## Setup Instructions

1. **Download the verify script file:**
Download the `VerifyPayianoWebhookSignature.js` script file to local machine.

2. **Install Node.js:**
Ensure Node.js is installed.

3. **Run the Script:**
Open a terminal or command prompt, navigate to the directory where the file is saved, and run the script using Node.js:

```shell
node verifyPayianoWebhookSignature.js
```

## Testing

The script will output the following information to the console:

- **getSignatureText**: The text used to compute the `HMAC` signature.
- **getComputedSignature**: The `HMAC-SHA256` signature computed from the payload and secret.
- **isVerifiedSignature**: Whether the computed signature matches the received signature.

If everything is set up correctly, you should see output similar to this:

```json
{
  "getSignatureText": "webhook_event.id=01j3521znn3b6wderr4vbyq18n&webhook_event.type=company.created&webhook_event.version=v1&webhook_event.fired_at=1722572118554&webhook_event_attempt.id=01j354j6nkwh3mdvhs6dsmswt8&webhook_event_attempt.sent_at=1722572118554&details.data.company.name=Graply URL Shortenr&details.data.company.avatar=null&details.data.company.is_active=true&details.data.company.is_approved=false&details.data.company.employees_count=0&details.data.company.owners.0.name=Amgad Yassen&details.data.company.owners.0.position=CEO&details.data.company.owners.0.percentage=51.5&details.data.company.owners.1.name=Kamal Allam&details.data.company.owners.1.position=CEO&details.data.company.owners.1.percentage=48.5&details.data.company.description=A leading company providing solutions for converting lengthy URLs into short ones & simplifying online sharing!&details.data.company.social_urls.facebook_url=https://facebook.com/graply&details.data.company.social_urls.linked_in_url=null",
  "getComputedSignature": "a621fc745416b00bb24758440fa75a850f6f8cb3f901217a6a9854f043ff8b70",
  "isVerifiedSignature": true
}
```

## Troubleshooting

- Ensure Node.js is correctly installed and configured.
- Double-check that the correct file path is being used when running the script.

## License

This project is open-source and available under the MIT License.