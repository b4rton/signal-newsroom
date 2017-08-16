# Using Signal as a Newsroom Dropbox
## Working draft 8/16/17
### By Barton Gellman
   
Journalists have made growing use of [Signal Private Messenger](https://whispersystems.org/) as a channel for confidential sources to make contact and share information. Simple precautions in the newsroom make for a much safer Signal dropbox. Sources may take their own additional precautions, not covered here. 
  
## Risks

Signal can make voice and video calls, but its main use as a newsroom dropbox is for text messages and attached documents. These present at least two kinds of risk.

1. Signal can carry malware, just as email can. An infected file or link may compromise the Signal account, the device used to log into the account, or a network connected to the device. 
2. Signal messages are strongly encrypted in transit, but not after they arrive. Incautious handling of information received may expose it to outside eyes.

## Precautions

A considered workflow in the newsroom can reduce those risks and limit the damage if the system is compromised.

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
	- Turn on local storage encryption -- FileVault on Mac, BitLocker on Windows. Choose a strong, random passphrase. [Don't bother](https://www.wsj.com/articles/the-man-who-wrote-those-password-rules-has-a-new-tip-n3v-r-m1-d-1502124118) with c@Ps&S6mb0l$. A randomly generated 7-word phrase is stronger and easier to type. Purists call for use of [actual dice](http://world.std.com/~reinhold/diceware.html), but you probably won't. So let 1Password or LastPass make a strong passphrase. In a pinch, even an [online generator](https://passwordcreator.org/diceware.html) is better than trying to think of "random" words yourself.
	- Install Chrome (Signal Desktop requires it) but do not use it for browsing.
	- Do not install or use any other software.
	
	c. Lock up the phone and computer as securely as possible when not in use.
	
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

4. **Transfer attachments. Don't open them.** There is no risk in reading Signal text messages, but do not click any link or open any file attachment on the same device that retrieves them.

	a. *Treat files and links received with Signal as malware.* Send them to another machine and open them there. 
	
	b. *Delete executable files upon receipt*. Those include extensions such as .exe, .sh, and .py. There are [many others](https://www.lifewire.com/list-of-executable-file-extensions-2626061).  
	
	c. *Set up a second computer as a secure workstation.* Configure it like the first one, then add the minimum software required to view files in standard formats such as PDF and Office. If practical (see next paragraph), disconnect the computer from internal newsroom networks and the Internet.
		
	d. *Move attachments securely to the workstation.* Once a file arrives on Signal, it is unencrypted. It cannot be safely transferred to another machine on an open channel such as email or Dropbox. In any case, you aren't running apps like those on the device that retrieves messages from the published Signal account.  
	
	- If you can place the secure workstation near the Signal Desktop machine, "airgap" the workstation. Switch off wifi, disconnect Ethernet cables, and consider removing the network hardware from the machine. Use an encrypted thumb drive or encrypted SD card to transfer incoming file attachments to the workstation. Reformat (erase) the thumb drive or SD card between uses. An SD card is safer. For maximum security, use an old digital camera or voice recorder to erase the SD card before and after each file transfer.
	- If you cannot keep the workstation near the Signal Desktop machine, connect it to a dedicated network, as described above. Create a second, unlisted Signal account for the workstation. Forward file attachments from the public Signal account to the unlisted one.
	
4. **View attachments safely.** To reduce the risk that malware will allow an attacker to exfiltrate files from the workstation, use one of these methods, listed in order of preference.

	a. Use an "airgapped" workstation, as described above. 
	b. Install a [Virtual Machine](https://lifehacker.com/5204434/the-beginners-guide-to-creating-virtual-machines-with-virtualbox) on the workstation. Switch off network access for the VM. Open attachments inside the VM, then use a "snapshot" to restore the VM to its original state. Remember to keep the VM software, including the guest operating system, up to date.
	c. Before opening an attachment or clicking a link, check it against the [VirtusTotal](https://www.virustotal.com) database of known malicious files and sites. Technically proficient users should send a "hash" of a file attachment, not the file itself. 
	d. [***With caveat***]: Open the attachment in Google Docs. This protects your workstation from malware, but exposes your confidential information to a subpoena or a thief who steals your login credentials.
	
5. **Safely distribute information to colleagues** When it comes time to share Signal content, save it in a safer format before allowing it onto a newsroom network. 

	a. Print the document (on a non-networked printer). 
	b. Copy and paste from an incoming Word or PDF attachment to a .TXT or .RTF file. 
	c. Save information from a spreadsheet in .CSV format.
	c. Use a screenshot to capture graphics. 
	d. If the content poses any risk to a source, share and store it encrypted.
	
*Comments, suggestions, corrections and criticism welcome*
	
  
