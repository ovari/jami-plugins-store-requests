# Extension Store Request Repository

This repository is used to request a certificate to be eligible for the [Extension Store](https://dl.jami.net/plugins) and upload new extension.

**Jami Extension Store** is a repository of extensions for the Jami client. It is a way for developers to share their extensions with the community.
It is also a way for users to securely find and install extensions.

## Request an organization certificate

To request a certificate for your organization, please open an issue with [this template](https://github.com/savoirfairelinux/jami-plugins-store-requests/issues/new?assignees=&labels=organization+plugins+store+request&projects=&template=organization-request.md&title=).

1. Create a new certificate signing request (CSR) for your organization with [Extension tool](https://git.jami.net/savoirfairelinux/jami-plugins).
2. Keep the private key and send the CSR to us with the command ```/csr <your-csr>.gz``` .
3. If the CSR is valid, a message will confirm that your certificate is ready to be check by our team.
4. If your CSR is not valid, a message will tell you to retry.
> Note: It's very recommended to use the Extension tool to create your CSR. If you use another tool,
please make sure that your CSR is valid with the command ```openssl req -text -noout -verify -in <your-csr>.gz``` and you use gzip compression.
4. If your organization is illegible, we will send you back your certificate signed by the ca.

## Submitting an extension

To request to upload an extension, please open an issue with [this template]().

1. Sign your extension with [Extension tool](https://git.jami.net/savoirfairelinux/jami-plugins) and your certificate.
If you don't have a certificate, please follow the steps to [request a certificate](#request-an-organization-certificate)
2. Please upload your extension in a source that can be fetch by anyone. To be sure, use this command:  curl -o tmp/plugin.jpl -L <url-to-fetch-file>
3. Please use the command to start the verification: /upload <url-to-fetch-file> as a comment in the issue
4. Wait until it respond successfully to the verification.
5. An administrator will upload your extension.

## Make a decision to upload an extension (Admin)

To accept or not to upload an extension, please follow the steps below.

1. Check that the extension is correctly sign and have the good access to the extension during the verification process
2. Verify the extension manually and check for any security issues
> Note: Jami is not responsible for the extension download by user.
3. Add a comment with the command '/accept' or '/decline' for the decision made

## More Information

For more information about the Extension Store, please visit the [Extension Store documentation](https://docs.jami.net/jami-extensions/).
