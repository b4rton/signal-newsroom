# Signal as a Newsroom Dropbox
## By Barton Gellman
*Updated 8/18/17. Comments welcome.*

Individual journalists have made increasing use of [Signal Private Messenger](https://whispersystems.org/) to talk to confidential sources. Ordinarily this requires a prior relationship and an exchange of mobile telephone numbers. News organizations have recently begun to repurpose Signal as a dropbox for tips from the general public to the newsroom at large. A single, newsroom-wide account, displayed prominently on a web site, offers potential sources a way to make first contact, find the right reporter and send information in relative safety. Signal's built-in features offer strong protections, but newsrooms can make it safer for source and journalist alike. This guide tries to strike a tolerable balance of security and usability. When the stakes are very high, a newsroom can do more. In time, based on expert suggestions I have already received, a more advanced guide may follow.
  
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
	- Do not store Contacts on the phone, even for Signal sources. In general, move source contacts and content to encrypted storage on another device. Delete those from the iPhone used for Signal as soon as practical. This limits the damage if the iPhone is stolen or lost.
	- Use the Settings app to harden the iPhone. 
		- In the first tab (AppleID, iCloud, iTune & App Store): Create a new AppleID. Log into iTunes & App Store. Turn on Automatic Downloads for Updates only. Do **not** log into iCloud. 
		- In Wi-Fi, turn on Ask to Join Networks. Do not join any network other than the one described in Section 3 below.
		- In Bluetooth, switch it off
		- In Cellular, turn on Cellular Data. Below that, disable it for every app but Signal. You will not see Signal on the list until you download it from the App Store.
		- In Control Center, turn off Access on Lock Screen
		- In General, scroll down to Restrictions. Disallow all apps and actions except for Camera and Installing Apps, which are needed to set up Signal. Confirm especially that Safari, Siri and AirDrop are disallowed.
		- In Display & Brightness, set Auto-Lock to 30 seconds
		- In TouchID & Passcode, set a [longer numeric PIN](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/) than Apple's 6-digit default, enroll no fingerprints, leave off all three options for TouchID, set Require Passcode to Immediately, turn off all options for Allow Access When Locked, turn on Erase Data after 10 failed attempts.
		- In Privacy, switch off Location Services. Later, you will say yes when Signal asks for access to the Microphone, Camera and (your empty) Contacts list.
		- In Mail, do not set up any account, including Google and any newsroom Exchange Server.
	- Open the App store and install Signal. Do not download any other apps.  
	- Do not use any app but Signal. Do not send ordinary text messages, browse the web or log into any online service. 
	- Do not use the iPhone for ordinary calls. Set an outgoing voicemail message to say the number is used only for private messages in the Signal app, which may be downloaded from whispersystems.org. 
	
	b. *Dedicated computer*
	
	- Set up a freshly wiped computer with the latest operating system. Turn on automatic updates.
	- Turn on the built in firewall, with strictest settings. 
	- Turn on local storage encryption -- FileVault on Mac, BitLocker on Windows. 
	- Create a strong login passphrase. [Forget the old advice](https://www.wsj.com/articles/the-man-who-wrote-those-password-rules-has-a-new-tip-n3v-r-m1-d-1502124118) to use c@Ps & syMb01$. A randomly generated 6-word phrase is stronger, more memorable and easier to type. Do not try to think of "random" words by yourself. Purists would have you use [actual dice](http://world.std.com/~reinhold/diceware.html) to pick from a word list, but a random phrase generated by 1Password, LastPass or [this site](https://www.dmuth.org/diceware/?debug=6) is more than strong enough for this purpose.
	- Install Chrome, Chrome's Signal Desktop extension, and no other software. Do not use Chrome for browsing.
	
	c. *When the devices are not in use*
	
	- Log off the computer, shut down the phone, and place them under lock and key. Signal will retrieve new messages when you turn them back on.
	
2. **Set Signal preferences**

	a. On the Signal iPhone app 

	- Tap the gear icon on the upper left to open Settings.
	- Under Privacy settings, switch on "Enable Screen Security" and switch of "iOS Call Integration." The latter keeps Signal voice calls off the Phone app's Recent list.
	- Under Notification settings, set Show to "No name or message." 
	- Each time a new source appears on your message list, tap the source's telephone number at the top of the screen and turn on "Disappearing Messages." Twelve hours is a reasonable default.
	- Delete each message thread entirely as soon as you have saved the contents and the source's telephone number elsewhere. You or your source can start a new thread whenever you like.
		
	b. On Signal Desktop

	- Tap the icon showing three stacked dots toward the top left of the message list. Choose Settings. Under Notifications, choose "Neither name nor message."
	- Each time a new source appears on your message list, click the icon showing three dots on the top right of the window. Turn on "Disappearing Messages." Messages will disappear on the source's device as well, so remind the source to save any information s/he needs somewhere else.
	- Delete each message thread entirely as you have saved the contents and the source's telephone number elsewhere. You or your source can start a new thread whenever you like..

3. **Use an isolated network.** 

	a. Do not connect the dedicated computer or iPhone to a network that is used by any other device. 
	
	b. On iPhone, use mobile data billed to the carrier's account. 
	
	c. On the computer, use a dedicated mobile wifi hotspot or an Ethernet cable to a dedicated router.

4. **Don't click links or open attachments** on the Signal smartphone or PC. Move them instead to another machine, then delete the originals.

	a. *Treat links and attachments as malware.* Above all you must protect the Signal device. 
	
	b. *Delete executable files upon receipt*. Trash any attachment with an extension such as .exe, .sh, or .py. There are many others. If you don't recognize a file type, check [here](https://www.lifewire.com/list-of-executable-file-extensions-2626061).
	
	c. *Set up a secure viewing workstation.* Configure and maintain a second computer as you did the first. Then install the bare minimum software required to view standard file formats such as PDF and Office.
		
	d. *Transfer attachments securely to the viewing workstation,* taking care not to expose the contents in an unencrypted state.
	
	- If you can place the workstation near the Signal Desktop machine, "airgap" the workstation. Switch off wifi, unplug any Ethernet cable, and consider removing the network hardware entirely. Use an encrypted thumb drive to move attachments from the PC running Signal Desktop to the workstation. Reformat (erase) the thumb drive before and after each transfer. For better security, use an encrypted SD card instead of a thumb drive, and erase it between uses with a basic digital camera or voice recorder.
	- If you cannot place the workstation near the Signal Desktop machine, connect the workstation to a dedicated Internet access point. Create a second, unlisted Signal account for the workstation. Forward file attachments from the public Signal account to the unlisted account. Alternatively, transfer attachments with [OnionShare](https://onionshare.org/). 
	
5. **Open attachments with care** on the workstation, using one or more of these options. 

	a. "Airgap" the workstation. An intruder cannot easily steal data from a machine that does not touch the Internet, even if the machine is compromised by malware. This is not an absolute defense, but it defeats many attacks.
	
	b. Install a [Virtual Machine](https://lifehacker.com/5204434/the-beginners-guide-to-creating-virtual-machines-with-virtualbox) on the workstation. Keep the host machine air-gapped, or switch off network access for the guest VM. Take a snapshot of the guest VM in its original, pristine state. Open attachments inside the VM, then restore from the snapshot. Install software updates, as available, on the VM, then save a new snapshot.
	
	c. Before opening an attachment or clicking a link, check it against the [VirtusTotal](https://www.virustotal.com) database of known malicious files and sites.
	
	d. [***With important caveat***]: Open the attachment in Google Docs. This protects your workstation from malware, but it places unencrypted data on Google servers, where it may be exposed by subpoena or a hacker who steals your log in credentials. 
	
6. **Save information in a safer format before sharing with colleagues.** This helps scrub malware and clues that might identify the source.   

	a. Print a document or excerpts on a non-networked printer. Shred it when no longer needed. 
	
	b. Copy and paste text from a Word or PDF document to a .txt or .rtf file. 
	
	c. Copy and paste data from an Excel spreadsheet to a .csv or tab-delimited textfile.
	
	d. Capture images and graphics in Adobe or Powerpoint format with a simple screenshot.
	
	e. Retype a document or message, rather than share the original.
	
	f. No matter how you share or store source material, keep it encrypted when not in active use.
		
/END	
  
