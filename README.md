# DigitalSignature
Uses the RSA encryption algorithm to sign a file/message, then allows you to check if the file/message has been altered.<br>

Program creates a public and private key using the RSA algorithm, then opens a file to sign.<br>
The signature is calculated from a SHA-256 hash of the original files contents, along with the public key.<br>
The signature is placed on the first line of the newly created file with the original file/message attached underneath.<br>
<br>
When attempting to verify if the message in the file has been altered, we use the private key to decrypt the signature,
which will return the hashed value of the original message.<br>
If the file has not been altered, the decrypted hash value should be identical to the remaining attached message
hashed with the SHA-256 algorithm. <br>
An output statement will tell the user whether or not the file has been altered. <br><br>

Command Line Arguments:<br>

To place your digital signature in a file: `projectMainSourceFile.java s <file-to-sign>` <br>
To verify that the file was not altered: `projectMainSourceFile.java v <file-to-verify>`
