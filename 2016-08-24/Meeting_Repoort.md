#Meeting minutes from Kreogist Dev Team meeting 24.8.2016

24, August, 2016

## Abstract
1. Report to Kyle.
2. Discuss about security content.
3. Discuss about the Receiving policy.
4. Fixed the Microsoft bug.

## Content
1. We will encrypt the sending E-mail using AES when stored at temporary file.
2. Use data will be encrypted via AES-256 using an independent password.
3. Find out the reason why SSL failed on Mac OS X platform.

This is wired problem. It works nice on both Linux and Windows. But only find out this bug on Mac. The problem is, on Mac OS X, it cannot communicate with the server via SSL protocol. But it could do with plain TCP without encrypt. It only works with ANU's Microsoft Outlook server.

The reason is that Microsoft forced to use TLSv1.0 or later, we set the SSL communication force to TLS1.0 or later, we changed it to compability with the older protocol version. It fixed. We provide a new option in the protocol configuration structure to store this setting.  