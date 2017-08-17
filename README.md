# Signal as a Newsroom Dropbox
## By Barton Gellman
*Updated 8/17/17. Comments welcome.*

Individual journalists have for some time been using [Signal Private Messenger](https://whispersystems.org/), which runs on most smartphones and desktop computers, for secure communications with their sources. In a more recent trend, news organizations have begun to repurpose Signal as a dropbox for the general public. Prominent display of a newsroom-wide Signal account number invites anyone with a confidential tip to make first contact, find the right journalist, send information, and develop an ongoing reporter-source relationship. Signal offers strong encryption and a measure of anonymity. Newsrooms can make it a safer channel with a few additional precautions. 
  
## Risks

Signal makes voice and video calls, but newsroom use has focused mainly on text messages and documents sent as attachments. These pose at least three kinds of risk.

1. **Malware.** Like email, Signal can transmit malicious attachments or web links. Sources may send malware unknowingly. If the newsroom's smartphone or PC is compromised, outsiders may be able to take control of the Signal account, send malware or false messages to sources, monitor communications without leaving obvious signs, or tunnel into any newsroom network that is reachable from the infected Signal device. 
2. **Exposure of content.** Signal messages are encrypted in transit but decrypted upon receipt. Incautious handling on the newsroom side may allow outside eyes to read Signal communications after they arrive.
3. **Exposure of sources.** In either of the first two scenarios, an adversary may learn enough to identify a confidential source by name, telephone number or job description.

## Precautions

A careful newsroom can reduce the risk and limit the damage of a successful intrusion into its Signal dropbox. Many of these precautions could do the same for journalists with individual Signal accounts.

1. **Secure the devices used for Signal**. 

	a. *Dedicated smartphone*. Run the Signal app on a freshly wiped iPhone. (Android phones are harder to secure.) 
	
	- Install iOS updates as soon as notice appears in the Settings app. 
	- Do not store Contacts on the phone, even for Signal sources. It is much safer to keep them elsewhere. If you must store source telephone numbers, list them under non-revealing pseudonyms such as "Source A" and "Source B." But really, don't.
	- Go through the Settings app to enhance privacy and security. Do NOT log into iCloud. (It will back up the Signal database.) Set a [longer numeric PIN](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/) and turn ON "Erase Data" after 9 failed unlock attempts. Disable most or all options under Lock Screen Access. Set Auto-Lock to 30 seconds. Turn OFF TouchID and Location Services. Create a new Apple ID with a throwaway email; you'll need it to download Signal from the App Store. Say yes when Signal asks for access to the Microphone, Camera and (your empty) Contacts list.
	- Install no software other than Signal. 
	- Do not use the iPhone for ordinary telephone calls, web browsing, email, taking or storing photos, or any other purpose. 
	- During Signal video calls, do not point your camera at anything that might reveal where you store the iPhone.
	
	b. *Dedicated computer*. Run Signal Desktop on a freshly wiped computer with the latest operating system. 
	
	- Set the computer to download and install updates automatically.
	- Turn on the built in firewall, with strictest settings. 
	- Turn on local storage encryption -- FileVault on Mac, BitLocker on Windows. Choose a strong passphrase. [Forget the old advice](https://www.wsj.com/articles/the-man-who-wrote-those-password-rules-has-a-new-tip-n3v-r-m1-d-1502124118) to use c@Ps & syMb01$. A randomly generated 6-word phrase is stronger, more memorable and easier to type. Don't try to think up a random phrase yourself. Humans are bad at that, and it matters. Purists say to use [actual dice](http://world.std.com/~reinhold/diceware.html), but you probably won't. So let 1Password or LastPass choose a passphrase, or make one [here](https://www.dmuth.org/diceware/?debug=6).
	- Install Chrome (Signal Desktop requires it) but do not use it for browsing.
	- Do not install or use any other software.
	
	c. Log off the computer, shut down the phone, and lock them in a physically secure space whenever you do not have eyes on them.
	
2. **Use secure Signal settings.**

	a. On the iPhone Signal app, in the message list view, tap the gear icon at the upper left for Settings. 

	- Under Privacy settings, switch ON "Enable Screen Security" and switch OFF "iOS Call Integration." 
	- Under Notification settings, set Show to "No name or message." 
	- Each time you view a message from a source, tap the source's name or number at the top of the screen and turn ON "Disappearing Messages." Twelve hours is a reasonable default.
	- Delete the entire message thread for each source as soon as you've saved the contents and the source's telephone number elsewhere. You don't need an existing thread to send or receive new messages.
		
	b. On Signal Desktop

	- Tap the icon showing three stacked dots toward the top left of the message list. Choose Settings. Under Notifications, choose "Neither name nor message."
	- Each time you view a message from a source, click the icon showing three dots on the top right of the window and turn ON "Disappearing Messages." 
	- Delete the entire message thread for each source as soon as you've saved the contents and the source's telephone nmber elsewhere. As on the iPhone app, you don't need an existing thread to send or receive new messages.

3. **Use an isolated network.** 

	a. Do not connect the dedicated computer or iPhone to a network that is used by any other device. 
	b. On iPhone, use mobile data. 
	c. On the computer, use a dedicated mobile wifi hotspot or an Ethernet cable to a dedicated router.

4. **Don't click links or open attachments** on the smartphone or PC that operates the Signal account. Transfer them instead to another machine.

	a. *Treat links and attachments as malware.* It's essential to keep the Signal device pristine. 
	
	b. *Delete executable files upon receipt*. Trash any attachment with extension .exe, .sh, or .py. There are many others. If you don't recognize a file type, check [here](https://www.lifewire.com/list-of-executable-file-extensions-2626061).
	
	c. *Set up a secure viewing workstation.* Configure and maintain a second computer like the first one (1b, above). Then install the bare minimum of additional software required to view standard file formats such as PDF and Office.
		
	d. *Transfer attachments securely to the viewing workstation,* then delete the originals.
	
	- If you can place the workstation near the Signal Desktop machine, "airgap" the workstation. Switch off wifi, unplug the Ethernet cable, and consider removing the network hardware. When the newsroom Signal account receives a file attachment, move it to the workstation on an encrypted thumb drive. Reformat (erase) the thumb drive between uses. For better security, use an SD card instead. Erase it before and after each use with an old digital camera or voice recorder.
	- If you cannot place the workstation near the Signal Desktop machine, connect the workstation to the Internet on a dedicated access point. Create a second, unlisted Signal account for the workstation. Forward file attachments from the public Signal account to the unlisted account.
	
5. **Open attachments with care** on the workstation, using one or more of these options. 

	a. "Airgap" the workstation. An intruder cannot easily steal data from a machine that does not touch the Internet, even if the machine is compromised by malware. This is not an absolute defense, but it defeats many attacks.
	
	b. Install a [Virtual Machine](https://lifehacker.com/5204434/the-beginners-guide-to-creating-virtual-machines-with-virtualbox) on the workstation. Keep the host machine air-gapped, or switch off network access for the guest VM. Take a snapshot of the guest VM in its original, clean state. Open attachments inside the VM, then restore the clean snapshot. Install software updates on the clean snapshot as they become available.
	
	c. Before opening an attachment or clicking a link, check it against the [VirtusTotal](https://www.virustotal.com) database of known malicious files and sites.
	
	d. [***With important caveat***]: Open the attachment in Google Docs. This protects your workstation from malware, but it places unencrypted data on Google servers. A subpoena or hacker might obtain it there. 
	
6. **Share information with colleagues in a safer format** to scrub potential malware.  

	a. Print the document (on a non-networked printer) and shred it when no longer required. 
	
	b. Copy and paste information received in Word or PDF format to a .txt or .rtf file. 
	
	c. Copy and paste information from an Excel spreadsheet to a .txt or .csv file.
	
	d. Capture images and graphics, for instance from Powerpoint, with a screenshot.
	
	e. Retype a short document or message rather than distribute the original.
	
	f. However you share the information, and wherever you store it, keep it encrypted when not in active use.
		
/END	
  
