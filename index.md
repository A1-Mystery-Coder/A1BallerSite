## Welcome to the A1UP Baller Installer Website

Here you'll find links to the latest version as well as instructions on how to use the tool.

## What is the baller installer for A1Up Pinball machines?
It allows the downloading and installation of updates to your Arcade1up pinball machine without the need for overwriting the entire emmc potentially degrading the performance of your hardware, it also preserves your high scores in the process.

Their method will overwrite the entire emmc performing several write executions potentially degrading performance of your PCB over time, our method will only ovewrite the single file you're updating meaning our method is safer and more reliable for the longevity of your hardware.

We do not condone piracy, as such you shouldn't install tables you do not own onto your Arcade1up cabinet, this is simply a tool allowing you to do the upgrade method without having to lose your high-scores.

Additionally because of the way we do things, we're also able to support OSX where Arcade1up currently does not; meaning we fill a gap they're unable to by allowing those who own Mac computers to still update their cabinets and make those Attack From Mars cabinets playable again where they previously were not and people aren't getting what they've paid for. Additionally, those with Macs who had contacted Arcade1up were simply told that they don't have any plans to support them in the future.

In otherwords, Arcade1up provided you with a broken product; released an update you couldn't use and then told you if you don't have a PC you're on your own sorry.

## What operating systems does this support?
Mac OSX, and Windows 10.

## How do I use this?
YouTube videos coming soon.

## If I use this will I lose my high-scores?
Nope, the way this was built you will not lose your high scores.

## Can this damage my cabinet/pinball machine?
Nope, in-fact this is more safe than the official update mechanism that Arcade1up themselves have released as it doesn't write as much data to the emmc. 

Like with Solid State Drives the more writes that occur the less life the emmc will have, well in order to write the data Arcade1up provides, it overwrites everything on the device meaning it does 1,000x more the writes we do to perform a simple update to a single file.


## This isn't working for me what can I do?
There is a troubleshooting guide included in the readme given, additionally we will be releasing updates to this to make it better for everyone.

## How does this work?
There's been a lot of speculation on how this works, and we're here to tell you that it actually has nothing to do with the Arcade1up process. This was happening long before the Arcade1Up updates had been released as we were testing out ideas with running custom code on PCBs to make them do more than they alerady did out of the box for instance running some retro game with retroarch or some other such thing.

How this actually works is it boots a custom built boot loader, kernel and file-system which establishes a USB ethernet gadget (RNDIS for windows), (CDC ECM for OSX) and allows your computer to then talk to the custom kernel over the network. Once that connectivity is established the custom boot loader and kernel have mounted the internal emmc of the device and allow access to the file system.

Some people have believed this some how borrowed from the method that Arcade1up relies on with flashing, in-fact it does not and the method it uses is technically much safer as it writes individual files while updating the system rather than attempting to overwrite the entire emmc storage. There have actually been several people that have had faulty hardware (Current guess is a power issue with the PMIC or the powersupply itself) where the Phoenix Tool (Allwinner Flashing tool) that Arcade1up has provided has lead to the bricking of the device because it only writes halfway before having an error.

Ultimately though, all of these methods on non-malfunction hardware should be safe as the Allwinner H6 chip included on the PCB has it's own software that isn't being overwritten by either of these methods, and is actually what is used to perform both methods. This programming interface was known about prior to Arcade1up releasing any information about it and was already being used to interface with the PCB.

## Is it safe?
If you read about how it works, you'll note that there is read-only software stored on the main SoC of the PCB the Allwinner H6. Because of the way this read-only software works it allows for the re-writing of your emmc and will prevent a permanent brick from ever occuring. In the event a Phoenix Tool write fails or this software fails to connect even the USB device of a network interface at all, the chances are that you have a faulty PCB and should get that warrantied by Arcade1Up.

## Is this legal?
Absolutely, you own the hardware that is being modified in this process and no intellectual property, trademarked properties, or copyrighted properties are distributed with this script or software. In no way can this be constituted as piracy on it's own, and nor does it violate any laws.

The act of modifying your own hardware is heavily covered under the right to repair, and protected by organizations like the EFF who would gladly back a cause like this one. You weren't given the necessary software to update your systems without damaging them further potentially leading to bricks, or even losing data that belongs to you (high scores). This ultimately improves and adds features to a process that already existed without breaking any kind of protections, digital rights management, or re-distributing non public-domain IP.

In-fact this is part of the reason this script gives you the exact same options Arcade1up already has, if you own a table download the update and install it; if you do not own the table you download then you're breaking the honor system Arcade1up has put fourth. This does nothing more than Arcade1up has already offered you except that it makes the process available to more people, does it in a safer manner and ensures you do not lose those high scores you worked so hard for.

Know your rights when it comes to hardware! Don't let suppliers and manufacturers bully you into thinking you're doing something wrong!

For more information on right to repair see: https://en.wikipedia.org/wiki/Electronics_right_to_repair

For more information on the Electronic Frontier Foundation see: https://www.eff.org/

## Was Arcade1up or anyone affiliated with them invovled in the development of this project, software or script?
No, Arcade1up has actually harmed consumers removing the original updates offered to add additional functionality to their cabinets as a result of this. They unfairly and unjustly have asked content creators on YouTube to remove videos related to this software,script and project claiming that it is piracy.

The actions committed by a user are outside of the control of the creators of this software, just as they were outside of the control of Arcade1up when they released their updates and people were flashing images to different tables they did not own. This software enables people to do with the Arcade1up software what they will do.

A torrent client isn't illegal or piracy on it's own because it allows for the downloading of content, the same rules and concept applies here. It is an individual user's actions that make things illegal or piracy not the software or script.

Arcade1up staff also believe this was only possible because updates were not 'keyed' to specific machines, this has nothing to do with updates or flashing or the fact full images were supplied. Again these tables and their PCBs have been wide open for the better part of a year, stop judging people in your private groups thinking they're sharing information about your update process like the publicly documented programming of an Allwinner H6 SoC was some private information.

Additionally, Arcade1up are responsible for conducting illegal activity and not following the compliance of software which they are using for commerical use. They violate the GPL licensing of several pieces of software including but not limited to U-Boot, Android OS, Linux and many others. They should be held accountable for these actions of profiting off of open-source works while not following the terms of the licenses.

It's amazing any license holders such as Zen Studios, Capcom, Sega, Raw Thrills or any others are wiling to work with a company that won't even follow the licenses of the open-source community themselves. How do you expect them to uphold the terms of your agreements when you license your software to them if they won't even comply with those of the software they get for free?

## Who are you? Do you work for Arcade1up?
At the moment we're a small team of people that believe hardware should be open and available to do what you wish with it, especially when you pay so much for it. Yes, there have been various childish rants and other things said and mentioned that has nothing to do with any of the above mentioned. That mostly has to do with disastisifaction with a community seeing people attempting to profit of of illegally modifying things.

If you do it on your own time, we don't condone it but understand it happens. Don't go and sell it though, you're making things worse.

No, we do not work for Arcade1up. No we do not have any inside knowledge of Arcade1up. No we have never worked for or with Arcade1up.

We simply understand how the open-source software, and hardware Arcade1up uses works and what they rely on and don't agree with their non-compliance to licensing models such as the GPL v2.

## Will you make modifications or hacks for other systems and PCBs?
Originally, this would've been it. Originally, this site wouldn't have existed.

Now, We're kind of annoyed by the reactions and giant fit thrown by one single Arcade1up employee who has vowed/guaranteed nothing like this would ever happen again. Now we're here to promise you it will.

If there are a generation 2 of pinball cabinets, or any other cabinets it will be our mission to develop modifications for them allowing you to use this hardware in the way you seek, in no way will that goal ever be to enable piracy but simply to allow you to run the software you want to on the hardware you personally own. This all being said, there are fun times ahead and we have a massive stack of different PCBs and a complete understanding how all of them as well as the future mediatek chips work.

We also have exploits in the open-source bootloaders you unfairly make use of without complying to the terms of the agreements of making use of that software, including those used by MediaTek. Good luck on your "this will never happen again"; We're here and we're not leaving.

## Why'd you make this, why does it let me run 30 tables on 1 cabinet if you don't condone or support piracy?
We made this to allow you to do what you wish with your hardware.

If you own all 30 tables there's no reason you shouldn't be able to run all 30 on a single cabinent, or all 3 cabinents even. As long as you're not making illegal copies of the software, which because you're downloading it from the Arcade1up service where they released the data into the public domain without proof of ownership being required and no terms of service that needed to be agreed to. You may not even be comitting piracy or breaking the law. Despite the fact they own the intellectual propery of portions of the data, as does Zen Studios. Arcade1up owns the license and has the ability to release the data legally as part of that agreement. However they also, made no committment to users to sign and or agree to an EULA or TOS. Therefore they were released into the public domain with no conditions or license restrictions being applied and thus are entirely legal to distribute, download and re-distribute under most circumstances, because of this they also have no right to revoke the license or precendence set forth because as a cabinet owner you were promised to be provided with these updates to correct issues with a faulty product you purchased and they agreed to correct.

The agreement they made was in-writting from those representing them as a company and organization via means of social media, where there were never any terms applied even verbally as to what you were able to do with the data or how you should be using it. No agreement was ever made on the consumer end, while Arcade1up made the agreement to produce the updates and are now trying to revoke that right and not honor the agreement they've made.

Despite that, at the end of the day. We don't support or condone piracy; remember, we didn't enable you to do anything other than what Arcade1up had already done we just made it easier to get your updated tables onto your PCB without losing data or having to reflash the entire thing potentially damaging the hardware of the emmc with unnecessary writes to 1,000 other files.

It's funny how Arcade1up has no problem with people making videos of running a PC in their system with a ton of pirated content, but a script that has a legimate use is suddenly an issue?

## Do you have a patreon or any other way to donate to you for creating this?
No, and we never will this isn't for monetary gain or finacial motive. This is to give the general population the freedom to do what they want with the hardware they own and paid close to if not over $1,000 for.
