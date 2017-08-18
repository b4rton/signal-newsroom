# Signal as a Newsroom Dropbox
## By Barton Gellman
*Updated 8/18/17*

[Signal Private Messenger](https://whispersystems.org/) has become a preferred channel of conversation between journalists and established confidential sources. Ordinarily, each must know the other's private telephone number in advance. News organizations have recently begun to repurpose Signal as a private gateway into the newsroom for potential sources who have no prior relationship there. By publishing a Signal telephone number for the newsroom at large, they enable anyone to make first contact, find the right reporter, and send information in relative safety. There are more sophisticated tools Signal is exceptionally easy to use and its built-in security is strong. A savvy newsroom can make it safer on both sides with precautions in its setup and use. This guide aims for a tolerable balance of security and usability, omitting steps I believe busy newsrooms unlikely to take. Comments, corrections and suggestions are welcome.
  
## Risks

Signal can make voice and video calls, but reporters and sources more commonly use it for text messages and transmission of documents. These pose at least three kinds of risk.

1. **Malware.** A source may send malicious links or attachments, knowingly or not. If successful in compromising the smartphone or PC used to manage the newsroom's Signal account, an intruder may be able to lock journalists out, read old communications, send fake messages or malware to sources, monitor live communications or tunnel into a newsroom's private network. 

2. **Exposure of content.** Though encrypted in transit, Signal messages are decrypted upon receipt. Incautious handling on the newsroom side may allow outside eyes to read Signal communications after they arrive.

3. **Exposure of sources.** In either of the first two scenarios, an adversary may learn enough to identify a confidential source by name, telephone number or job description.

## Precautions

The manager of a newsroom's Signal account can greatly reduce the risk and limit the damage of a successful intrusion

1. **Secure the devices used for Signal**

	a. *Dedicated iPhone* 
	
	- Set up a freshly wiped iPhone (Android is harder to secure). Apply updates promptly. 
	- Do not store Contacts on the phone, even for Signal sources. Doing so would be especially damaging if you inadvertently synced iPhone data with an online service.
	- In general, keep as little information as possible on the Signal device. Copy messages and source identifiers to encrypted storage elsewhere, then delete them from the iPhone. This limits the potential damage in case of loss or theft.
	- Use the Settings app to harden the iPhone. 
		- In the first tab (AppleID, iCloud, iTune & App Store), create a new AppleID. Log into iTunes & App Store, without which you cannot download Signal. Turn on Automatic Downloads for Updates only. Do **not** log into iCloud. 
		- In Wi-Fi, turn on Ask to Join Networks. Do not join any wifi network, except as described in Section 3 below.
		- In Bluetooth, switch it off
		- In Cellular, turn on Cellular Data. Scrolling down, disable cellular data for every app on the list. When you install Signal, it should have cellular data access by default. Come back to this setting and check.
		- In Control Center, turn off Access on Lock Screen
		- In General, scroll down and tap on Restrictions. Set a PIN when asked. Disallow all apps except for Camera. (The switch should be on the left, not the right.) Allow Installing Apps, but come back and switch that off after you install Signal. Confirm especially that Safari, Siri and AirDrop are disallowed.
		- In Display & Brightness, set Auto-Lock to 30 seconds
		- In TouchID & Passcode, set a [longer numeric PIN](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/) than Apple's 6-digit default. Enroll no fingerprints, switch off all three options for TouchID, set Require Passcode to "Immediately," switch off all options under Allow Access When Locked, and turn on Erase Data after 10 failed attempts.
		- In Privacy, switch off Location Services. Later, say yes when Signal asks for access to the Microphone, Camera and (the empty) Contacts list.
		- In Mail, do not set up any account, including Google and any newsroom Exchange Server.
	- Open the App store. Download Signal. Do not download any other app, now or later.  
	- Do not use any app but Signal, including Apple's. Do not make cellular phone calls. Set voicemail to inform callers that they have reached a Signal-only phone. Do not use Messages or try to browse the web.
	
	b. *Dedicated computer*
	
	- Set up a freshly wiped computer with the latest operating system. Turn on automatic updates.
	- Turn on the built in firewall, with strictest settings. 
	- Turn on local storage encryption -- FileVault on Mac, BitLocker on Windows. 
	- Create a strong login passphrase. [Forget the old advice](https://www.wsj.com/articles/the-man-who-wrote-those-password-rules-has-a-new-tip-n3v-r-m1-d-1502124118) to use c@Ps & syMb01$. A randomly generated 6-word phrase is stronger, more memorable and easier to type. Do not try to think of "random" words by yourself. Purists would have you use [actual dice](http://world.std.com/~reinhold/diceware.html) to select from a word list, but a random phrase generated by 1Password, LastPass or [this site](https://www.dmuth.org/diceware/?debug=6) is more than adequate here.
	- Install Chrome, Chrome's Signal Desktop [extension](https://chrome.google.com/webstore/detail/signal-private-messenger/bikioccmkafdpakkkcpdbppfkghcmihk?hl=en-US), and no other software. Do not use Chrome for browsing. 
	- Do not set up online accounts. Do not use built-in apps, especially email clients and web browsers. The machine is strictly for Signal.
	
	c. *When the devices are not in use*
	
	- Log off the computer, shut down the phone, and place them under lock and key. Signal will retrieve new messages when you turn them back on.
	
2. **Set Signal preferences**

	a. On the Signal iPhone app 

	- Tap the gear icon on the upper left to open Settings.
	- Under Privacy settings, switch on "Enable Screen Security" and switch of "iOS Call Integration." The latter keeps Signal voice calls off the Recent list in the Phone app.
	- Under Notification settings, set Show to "No name or message." 
	- Each time a new source appears on your message list, tap the source's telephone number at the top of the screen and turn on "Disappearing Messages." Twelve hours is a reasonable default. Warn the source that messages will disappear from his or her device, not just yours.
	- Delete each message thread entirely as soon as you can save the information you need somewhere else. You or your source can start a new thread whenever you like.
		
	b. On Signal Desktop

	- Tap the icon showing three stacked dots toward the top left of the message list. Choose Settings. Under Notifications, choose "Neither name nor message."
	- Follow the same steps as for iPhone to turn on Disappearing Messages and delete each message thread as soon as practical.

3. **Use an isolated network.** 

	a. Do not connect the dedicated computer or iPhone to a network that is used by any other device. 
	
	b. On the computer, use a dedicated mobile wifi hotspot or an Ethernet cable to a dedicated router
	
	c. On iPhone, use a dedicated mobile wifi hotspot or cellular data.

4. **Treat links and attachments as malware. Move them off the Signal device before opening.**
	
	a. *Before anything else, delete executable files upon receipt*. Trash any attachment with executable format such as .exe, .sh, .bat, .py or one of the [many other possibilities](https://www.lifewire.com/list-of-executable-file-extensions-2626061). Do not be fooled by misdirection such as "Readme.docx.exe." The real extension comes last.
	
	b. *Set up a secure workstation to view and work with Signal attachments.* Configure a second computer with the same settings as the first. Then install the bare minimum software required to open standard file formats such as PDF and Microsoft Office.
		
	c. *Transfer attachments securely to the viewing workstation,* taking care not to expose the contents in an unencrypted state.
	
	- If you can place the workstation near the Signal Desktop machine, "airgap" the workstation. Switch off wifi, unplug any Ethernet cable, and consider removing the network hardware entirely. Use an encrypted thumb drive to move attachments from the Signal Desktop machine to the workstation. Reformat (erase) the thumb drive before and after each transfer. For better security, use an encrypted SD card instead of a thumb drive.
	- If the workstation is far from the Signal Desktop machine, connect it to a dedicated Internet access point. Create a second, unlisted Signal account for the workstation. Forward file attachments from the public Signal account to the unlisted account. Alternatively, transfer attachments with [OnionShare](https://onionshare.org/). 
	
5. **Reduce the risk of infecting the workstation with one or more of these methods** 

	a. "Airgap" the workstation. An intruder cannot easily steal data from a machine that does not touch the Internet, even if the machine is compromised by malware. This is not an absolute defense, but it defeats many attacks.
	
	b. Install a [Virtual Machine](https://lifehacker.com/5204434/the-beginners-guide-to-creating-virtual-machines-with-virtualbox) on the workstation. Switch off network access for the guest VM. Take a snapshot of VM in its original, pristine state. Open attachments inside the VM, then restore the snapshot.
	
	c. Before opening an attachment or clicking a link, check it against the [VirtusTotal](https://www.virustotal.com) database of known malicious files and sites.
	
	d. [***With important caveat***] Open the attachment in Google Docs. This protects your workstation from malware, but it places unencrypted data on Google servers, where it may be exposed to subpoena or theft by hackers.
	
6. **Scrub malware and metadata by saving information in a simpler format**   

	a. Print a document on a non-networked printer. Shred it when no longer needed. 
	
	b. Copy and paste text from a Word or PDF document to a .txt or .rtf file. 
	
	c. Copy and paste data from an Excel spreadsheet to .csv or tab-delimited text.
	
	d. Capture images and graphics from Powerpoint in a screenshot.
	
	e. Retype instead of sharing an original document.
	
	f. Regardless how you share source information, encrypt it when not in use. 
		
END	
  
