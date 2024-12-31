---
layout: post
title:  "What end-to-end encryption actually means"
---
![Encryption Process](/assets/encryption.jpg)
#### **Preliminaries** -  
##### **Message** - Information that you want to send to someone
##### **Plain Text** - Information in the form that you and receiver can read and understand easily.
##### **Cipher Text** - Information in such a form that it cannot be understood or read.
##### **Encryption** - Process of converting plain text into Cipher text
##### **Decryption** - Process of converting Cipher text back into plain text
##### **Key** - A piece of data needed to encrypt or decrypt messages
##### **Private Key Cryptography** - A type of cryptography in which the same key is used to both encrypt and decrypt the message
##### **Public Key Cryptography** - A type of cryptography in which different keys are used for encryption and decryption

End-to-end encryption basically means that once you type and send your data to anyone, before being sent out of your phone into the internet, the data will be encrypted using the encryption key of the recepient. The process goes on as following -
1. When you begin a chat process with a recepient, WhatsApp will initiate a Handshake.
2. Both users will send each other their public encryption keys, for which they will each have the corresponding private key kept safe in the devices.
3. When one user sends a message, it will be encrypted using the recepient's public key received during Handshake.
4. Upon receiving the Cipher Text, recepient will use its decryption key i.e. the Private Key to decrypt the message.

How the seperate encryption and decryption keys are generated so that message encrypted with the encryption key can only be decrypted with the corresponding decryption key is related to rigorous mathematics involving Prime numbers. To learn more about it, read about the RSA algorithm [here](https://muirlandoracle.co.uk/2020/01/29/rsa-encryption/).

So end-to-end encryption does not mean that WhatsApp cannot see your messages. It just means that the message does not leave your phone without being coverted into a Cipher Text. So, if in future a new feature is rolled out which can use AI to generate appropriate Quick responses for certain messages, it does not mean that WhatsApp is leaking your data. It is just the Plain Text message on your device being used by an AI model to generate appropriate responses.