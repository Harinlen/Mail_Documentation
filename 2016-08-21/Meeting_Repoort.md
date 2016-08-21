#Meeting minutes from Kreogist Dev Team meeting 21.8.2016

21, August, 2016

1.How to store the folder information?

 Depends on: Cache mail or not?

Cache
-----
Advantage:

1. Read mail offline.
2. Quick access, reduce the usage of network. [*]

Disadvantage:

1. Disk usage increase a lot.
2. Synchronism issues.
3. Delete problem. [Hash Table]

We must cache the mail.

How to
------
Disk Tree view:

	abc@gmail.com
	┣Inbox
	┋┣Information
	┋┣hash1.eml
	┋┣hash2.eml
	┋┣hash3.eml
	┋┣...
	┋┗...
	┣Sent
	┗...

Sync
----
Must has a hash list [hash1, hash2, ...]

Fetch 50 mails when user 'list' 50 mails.

After download one mail, parse one mail.



**Breakthough!!!!!!!!**

We found the UID function in the IMAP. It provides the Unique ID of the mail.

We could use this instead of the ID.
