# Using Signal as a Newsroom Dropbox
## Working draft 7/31/17
### By Barton Gellman
   
Journalists have made growing use of [Signal Private Messenger](https://whispersystems.org/) as a channel for confidential sources to make contact and share information. Modest precautions on the newsroom side can make a Signal dropbox more secure. Sources may also take additional precautions, not covered here. 
  
## Risks

Signal can make voice and video calls, but its main use as a newsroom dropbox is to send text messages and attached documents. These present at least two kinds of risk.

1. Signal can carry malware, just as email can. An infected file or link may compromise the Signal account, the device used to log in to the account, or any network to which the device is connected. 
2. Insecure handling of information received by way of Signal can expose the information to outside eyes as though it had not been encrypted at all.  

## Precautions

A mindful workflow in the newsroom can protect against compromise and limit the damage of a breach.  

1. **Secure the devices used for Signal**. 

	a. Run the Signal smartphone app on a freshly wiped iPhone. (Android phones are harder to secure.) Keep iOS updated. Install no software other than Signal and do not use the phone for browsing, email or any other purpose. 
	
	b. Run Signal Desktop on a freshly wiped, dedicated computer with the latest updates installed. Turn on the built in firewall, with strictest settings. Install Chrome and the Chrome Signal app. Do not install or use any other software. Do not use Chrome for browsing.
	
	c. Lock up the phone and computer when not in use.

2. **Use an isolated network.** Do not connect the computer or the iPhone that run Signal to a network that is used for anything else. On iPhone, use mobile data. On the computer, use a mobile wifi hotspot or ethernet to a dedicated router. ***{Question for reviewers: Should I suggest a VPN as well?}***

3. 	**Transfer attachments to another machine** 

	a. *Treat files received with Signal as malware.* Do not open them on the same device that connects to the Signal account. Delete any executable file upon receipt. Those include extensions such as .exe, .sh, and .py. There are [many others](https://www.lifewire.com/list-of-executable-file-extensions-2626061).
	
	b. *Set up a second computer as a secure workstation.* Configure it like the first, then add as little software as possible to view files in standard formats such as PDF and Office.
		
	c. *Use an encrypted method to transfer attachments to the workstation.* 
	
	- If the workstation is near the Signal Desktop machine, leave the workstation disconnected from the Internet. Transfer files to the workstation on an encrypted thumb drive or (safer) an encrypted SD card. Wipe the thumb drive or SD card between uses.
	- If the workstation is elsewhere, connect it to a dedicated network. Create a second, unlisted Signal account. Set up Signal Desktop with the unlisted account on the workstation. Forward files from the public Signal account to the unlisted one.
	
4. **View and distribute attachments**

	a. *Reduce the risk of malware on the workstation.* In order of preference:	
	- Use an "airgapped" workstation, disconnected from all networks. 
	- Install a [Virtual Machine](https://lifehacker.com/5204434/the-beginners-guide-to-creating-virtual-machines-with-virtualbox) on the workstation. Switch off network access for the VM. Open attachments inside the VM, then restore a safe snapshot.
	- Before opening an attachment or clicking a link, check it against the [VirtusTotal](https://www.virustotal.com) database of known malicious files. Technically proficient users should send a "hash" of the file, not the file itself. 
	- [***With caveat***]: Open the attachment in Google Docs. This protects your workstation from malware, but potentially exposes confidential information to a subpoena or a thief who steals your login credentials.
	
	b. *Use a safer format to share information.* When distributing information to colleagues, share a file's contents instead of the file itself. Print the document (on a non-networked printer). Copy and paste from Word or a PDF, which can carry malware, to a .TXT or .RTF file. Use a screenshot to capture graphics from a PDF or Powerpoint file. And use encryption to transmit the sanitized file.
	
  
