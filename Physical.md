remote_theme: pages-themes/hacker@v0.2.0
plugins:
- jekyll-remote-theme # add this line to the plugins list if you already have one

#todo/methodology/physical
- [ ] Refine
# Prerequisites
- Is social engineering involved, or is it an escorted assessment?
- Is RFID cloning included?
- Has the Get Out Of Jail (GOOJ) Letter been completed?
- Are there contact details to provide should the GOOJ not be prepared?
- Have a background story or two for when asked about your purpose on site
	- I’m here to perform a network test, as [SITE MANAGER] reported that the Wi-Fi has been slow; if you’re able to point me in the direction of the comms room, I’m usually working at the [OTHER BRANCH] office, but I got a last-minute call to come here. 

# Passive Reconnaissance 
- Google Maps / Street View – View the client building
- Check for external doors, including maintenance entrances
- Check for internal doors – identify where staff may go
- Check for barriers or RFID pads
- Check for CCTV – How many cameras are visible
- Check for reception – Where is it located
- Check foot traffic – Is the area busy or empty
- Check for staff members – Are lanyards or fobs worn?-
- Gather names of management
	- Use the company website or LinkedIn to get the names of managers working at the testing location or site managers off-site.

# Active Reconnaissance
- Confirm CCTV locations
- Are staff members wearing the lanyards/fobs?
- If you have a similar style, wear it to blend in
- Are the RFID barriers working?
- Are staff ensuring external doors are closed behind them?
- Are staff members communicating on approach to the door or keeping heads down?

# Methods of entry
## Tailgating
 - Follow a staff member through the external door, allowing them to use their card access – best performed from 8:30 am – 9:15 am.
 - Having hands full may convince people to open the door for you, such as a coffee cup and a bag – A coffee cup can be empty, contain a device or have coffee.
- Parcel Delivery
	- Businesses typically have parcels delivered from 10-11 am. Reception can unlock the door; with timing, entry can be gained, and the receptionist could be busy with the delivery driver.
- Maintenance / Staff door
	- Buildings sometimes have an alternative entrance specifically for maintenance crew or staff.

# What to test
- How long till maglocks engage
- Do the emergency door release work
- Does an alert get sent to the appropriate people?
- Alert that it has been engaged – If not, the door could remain unlocked
- Is access control monitored
- Are keypads used? – No trace of who accessed
- Are RFID cards used? – Is the card ID unique to each staff member?

## Security Awareness
- Are staff members asking for confirmation of who you are?
- Are you being actively questioned?
- With permission from the client, how far can you act suspiciously?

## CCTV

 - Where is the footage stored, and for how long?
 - Is it actively monitored?
 - Locate critical Infrastructure and assess access controls
	 - Comms room
	 - CCTV Storage
	 - Server rack
- LAN Ports – Are there LAN ports out in the open, are they live – Tools like the SharkJack are good to test these on the fly.
- Unlocked computer 
- Unlocked cabinets

## Gather Information
- MAC Addresses – IP phones and printers are a good way to get MAC addresses
	- IP Phones – On the back
	- Printers – If possible, print a test page

## Sensitive information
- Wi-Fi passwords on posters
- Passwords on sticky notes
- Client information on Whiteboards

## USB Drops
- If in scope, prep USB flash drives to drop around the building, noting the placement. Then after a set amount of time, return to the locations to see whether the USB flash drives are present, have been handed in or have gone missing.

# What to do if caught
- **Stay calm.** 
- Can the situation be talked out before revealing the plan – Use your best judgement
- Have an ID and the GOOJ letter accessible – advise they can confirm with the contact.
- Answer any questions associated with the assessment
- Wait for the situation to be confirmed.
- If only a few staff members are aware of the assessment, advise that it can continue to assess the security awareness of other staff members; often, the reception has a shift change, allowing for another attempt to gain entry.


# Tools

## Ethernet
Gear that can be plugged into Ethernet ports to perform tasks
- [[SharkJack]] / HAK5: https://shop.hak5.org/products/shark-jack
	- Once plugged in, can perform scripts/commands such as running nmap 
	- ~15 minute battery, though can die quickly
	- LEDs

## BadUSB
Gear that can be plugged into USB ports to act as keyboards, typing at 'super human speeds'
- Digispark / Arduino: https://macrosec.tech/index.php/2021/06/10/creating-bad-usb/
	- Very cheap
	- Can have a single script compiled onto the device
	- Script is fired each time a connection is made
- [[BashBunny]] / HAK5: https://shop.hak5.org/products/bash-bunny
	- Can be used to mimic a BadUSB, Mass Storage and Ethernet adaptor
	- Can run one of two scripts or be placed in arming mode using the external switch
	- Much bigger than the average looking USB, not good for a USB Drop
- [[USB Rubber Ducky]]: https://shop.hak5.org/products/usb-rubber-ducky-deluxe
	- Runs script on connection
	- Houses scripts on SD card
	- looks like a USB flash drive
- Malduino W / Maltronics: https://maltronics.com/collections/malduinos
	- Fires off a script on connection, however can have several stored on it
	- Wi-Fi connectivity, allowing the use of launching more scripts using webUI
	- Has both USB A and USB C connector
	- LEDs
- P4wnP1 A.L.O.A / Raspberry Pi Zero W: https://github.com/RoganDawes/P4wnP1_aloa
	- Provides the Pi Zero W with similar functionality to the BashBunny
	- Provides Wireless connectivity
	- Not covert

## Lock Picking
Generally lock picking doesn't come up often, however if in scope, pick which is more appropriate for the job

### Covert
A simple wallet sized container is best to ensure that it's lightweight and not obvious when looking at
https://www.ukbumpkeys.com/products/credit-card-pick-set?variant=303601499

### Full Set
Should a full set be required, a variety of picks can allow for better success rates
https://www.ukbumpkeys.com/collections/lock-pick-sets/products/dangerfield-praxis-dual-gauge-21-piece-complete-lock-pick-set

## RFID

### RFID Cloning
- [[Flipper One]]: https://flipperzero.one/one
	- Light weight
	- Battery Powered
	- Covers a range of RFID frequencies
- ICopy-X: https://icopyx.com/
	- Light weight
	- Battery Powered
	- Covers a range of RFID frequencies
	- Can clone within 30 seconds for most cards
	- Can be updated with new keys
	- Has a PC mode to allow for more usability
- Chameleon Pro
	- Light weight
	- Can clone UIDs fast
	- Can store several UIDs and switch between

## Lanyards
- A collection of Lanyard
	- Colours
	- Styles
	- ID Holders

## Fobs
- A collection of fobs.
	- Colours
	- Styles

## USB Drops
Standard flash drives work for this, depending on the plan, usually =<2GB capacity, as it's likely to only house a small script and it'll be cheaper on bulk buy the smaller the capacity you go.
- USB Drop Script: https://github.com/Zetascrub/USB-Drop

## Fake Business Cards
- A Fake business card could be used to further solidify false identity
	- If a number is added, ensure that the number can be reached, there doesn't have to be an answer, a burner SIM can be used with a custom voice mail message, just something so further solidify a backstory

## Wi-Fi
- [[Wifi Pineapple Mk7]] / HAK5: https://shop.hak5.org/products/wifi-pineapple
	- Rogue Access Points
	- Automate capturing Handshakes
	- C2 Platform
	- Requires 5Ghz module.
- Alfa Cards: https://www.wifi-antennas.co.uk/alfa-awus036ach-1200-mbps-ultra-range-wifi-usb-adapter
	- Can be used for Wi-Fi assessments
	- Covers both 2.4 and 5Ghz bands

## Note Taking Tool With Sync Feature
- Joplin / Onenote / Obsidian
	- Have a note taking tool on your phone allowing you to look up notes in a more casual manner, rather than looking at a laptop, especially prior to approaching a building.
		- Checking notes from Passive Recon
			- Names
			- Job Titles

## Glasses
Study shows that people who are wearing glasses are trusted more, they don't have to be prescription glasses, could be off the shelf reading glasses or blue filters.

## Camera
Often taking pictures are useful for documentation within the report.
 - Phone
 - Hidden camera in glasses / pen

## Comms
When on site with at least one other colleague, it's useful to have communication between the two should there be any separation. Allowing one person to enter the building, verbally say details "Corridor on the right, looks like two doors are open" and the other to make notes, in case the first attempt has failed, the second attempt done by the other colleague can have notes. Also useful if one acts as a watch guard.
- Radios with covert ear pieces
- Mobiles with extensive minutes and ear piece.

## Radio
While unlikely to really help, it's possible to listen to radio chatter for potential useful information

## Drop Box
A device that can be plugged into the network which calls back to a C2 server, allowing for remote testing.
