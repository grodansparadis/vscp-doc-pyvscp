# Introduction



This specification is a reference document. With +500000 characters written by someone that is not native in English it may be a pain to read for many. If you just want to use VSCP & Friends skip to section 2. Go back to the specification when you are in doubt about usage or just need a deeper understanding of whats going on. VSCP is designed to make complex systems simple to use and not necessarily easy to build such complex systems. We expect a greater technical knowledge and at least the ability to read from people that build and maintain such systems. 



Another resource for information is the [VSCP wiki](ttp://www.vscp.org/wiki/doku.php\) it holds a lot of useful information and howto's. 

*  The VSCP Daemon is documented [here](http://www.vscp.org/docs/vscpd/doku.php).



*  The helper library is documented \[here\]\(http://www.vscp.org/docs/vscphelper/doku.php\)



*  The VSCP Works is documented \[here\]\(http://www.vscp.org/docs/vscpworks/doku.php\).



\#\# Introduction



VSCP is an open source standard protocol for m2m, IoT and other remote control and measurement applications. It enables simple, low-cost devices to be networked together with high-end computers and/or to work as an autonomous system, whatever the communication media is.



There are a lot of technologies and protocols that claims to be the perfect solution for \(home\) automation and SOHO \(Small Office/Home Office\) control, IoT, M2M. More and more RF solutions are now available: Bluetooth, Zigbee, Z-wave, Wifi, etc. Other systems use a dedicated bus based on RS-485, CAN, LIN, LON, TCP/IP, etc. or can sometimes support different transport layers: CANopen, KNX \(EIB\), C-Bus, LonWorks, etc.



Most of them are proprietary, some are somehow “open”, meaning you can participate if you are part of the alliance and pay your yearly fees, or similar. There also is small companies that have their own proprietary and completely closed protocols.



VSCP was designed with the following goals in mind:





\*  Free and Open. No usage, patent or other costs for its implementation and usage. 



\*  Low cost. 



\*  K.I.S.S. \(Keep it simple stupid.\) Simplicity usually rules. 



\* Discovery and identification. Installed devices should be possible to discover and be identified in an uniform way.



\*  Uniform device configuration. Devices should be able to be configured in a uniform way.



\*  Autonomous/distributed device functionality.



\*  Uniform way to update/maintain device firmware.



Some features: 





\*  Free and open for commercial and other use. 



\*  Have two levels. Level I and Level II where level I is designed with CAN as the least common denominator. Can be used for TCP, UDP, RF, Mains communication, etc etc. 



\*  Has globally unique IDs for each node. 



\*  Has a mechanism to automatically assign a unique ID to a newly installed node and inform other nodes and possible hosts that a new node is available and ready. 



\*  Use “registers” as a uniform way to configure nodes. 



\*  Can use a “decision matrix” to program nodes with dynamic functionality. 



\*  Has a common specification language “MDF” that describe a module in a uniform way that can be used by set up software and such. 



\*  Has software and drivers for Windows and Linux. More added all the time. 



The VSCP Protocol was initially used in CAN networks. CAN is very reliable and cheap today and allow us to manufacture low cost nodes that can work reliably, efficiently and can be trusted in their day-to-day use. But VSCP can be used equally well in other environments than CAN.



To meet both low cost and performance, VSCP is divided into 2 levels. Level 1 is intended for low-end nodes \(i.e. based on tiny micro-controllers\) while Level 2 is intended for higher level and faster transport layers such as TCP/IP. All nodes can talk together but level 2 nodes achieve better performance when talking together, while level 1 nodes that don't require much processing can be implemented with very cheap technologies.



Furthermore, VSCP:





\*  uses standard components and cables. 



\*  is easy to configure.



\#\# Open? What does that mean?



This protocol is open and free in all aspects that are possible. We want you to contribute work back to the project if you do your own work based on our code but we also like to make as much of this work useful also in commercial projects. The tool we have chosen to do this is the GNU public license and the lesser GPL. For firmware code we use an even more open model so that there is no question that you are allowed to put the code in your own commercial projects if you feel to do that.



The GPL license and the LGPL license is included in the distribution of code in the file COPYING but can also be ordered from by writing to the Free Software Foundation, 59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.



There is an exception in the license from GPL/LGPL that make the tools more useful for commercial use.



\#\# License



Alternative licenses for VSCP & Friends may be arranged by contacting \*\*Grodans Paradis AB/Paradise of the Frog\*\* at \[info@grodansparadis.com\]\(info@grodansparadis.com\), \[http://www.grodansparadis.com\]



\#\#\#\#\# License options



VSCP & Friends is licensed under three different licenses.





\*  Commercial users can buy a license from Grodans Paradis AB. 



\*  Non commercial users can use the GPL version. 



\*  Both commercial and non-commercial users can use the LGPL code such as libraries and firmware code.



\#\#\#\#\# Open License



As of February 2006, VSCP & Friends is released under a modified version of the well known GNU General Public License \(GPL\), now making it an official GPL-compatible Free Software License. An exception clause has been added to the VSCP & Friends license which limits the circumstances in which the license applies to other code when used in conjunction with VSCP & Friends. The exception clause is as follows:



\*As a special exception, if other files instantiate templates or use macros or inline functions from this file, or you compile this file and link it with other works to produce a work based on this file, this file does not by itself cause the resulting work to be covered by the GNU General Public License. However the source code for this file must still be made available in accordance with section \(3\) of the GNU General Public License.\*



This exception does not invalidate any other reasons why a work based on this file might be covered by the GNU General Public License.



The goal of the license is to serve the VSCP & Friends user community as a whole. It allows all VSCP & Friends users to develop products without paying anything, no matter how many developers are working on the product or how many units will be shipped. The license also guarantees that the VSCP & Friends source code will always be freely available. This applies not only to the core VSCP & Friends code itself but also to any changes that anybody makes to the core. In particular, it should prevent any company or individual contributing code to the system and then later claiming that all VSCP & Friends users are now guilty of copyright or patent infringements and have to pay royalties. It should also prevent any company from making some small improvements, calling the result a completely new system, and releasing this under a new and less generous license.



The license does not require users to release the source code of any applications that are developed with VSCP & Friends. However, if anybody makes any changes to code covered by the VSCP & Friends license, or writes new files derived in any way from VSCP & Friends code, then we believe that the entire user community should have the opportunity to benefit from this. The license stipulates that these changes must be made available in source code form to all recipients of binaries based on the modified code, either by including the sources along with the binaries you deliver \(or with any device containing such binaries\) or with a written offer to supply the source code to the general public for three years. It is perhaps most practical for VSCP & Friends developers to make the source code available online and inform those who are receiving binaries containing VSCP & Friends code, and probably also the VSCP & Friends maintainers, about the location of the code. See the full text of the GPL for the most authoritative definition of the obligations.



Although it is not strictly necessary to contribute the modified code back to the VSCP & Friends open source project, we are always pleased to receive code contributions and hope that developers will also be keen to give back in return for what they received from the VSCP & Friends project completely free of charge. The VSCP & Friends maintainers are responsible for deciding whether such contributions should be applied to the public repository. In addition, a copyright assignment is required for any significant changes to the core VSCP & Friends packages.



The result is a royalty-free system with minimal obligations on the part of application developers. This has resulted in the rapid uptake of VSCP & Friends. At the same time, VSCP & Friends is fully open source with all the benefits that implies in terms of quality and innovation. We believe that this is a winning combination. 



\#\#\#\#\# Commercial License



You have the right to incorporate any code of VSCP & Friends in your own application and resell it without any need to re-share any code.



The commercial licenses is available from \*\*Grodans Paradis AB/Paradise of the Frog\*\*, \[info@grodansparadis.com\]\(info@grodansparadis.com\). 



\#\#\#\#\# Questions and answers



The following queries provide some clarification as to the implications of the VSCP & Friends license. They do not constitute part of the legal meaning of the license.





\*  Q. What is the effect of the VSCP & Friends license?



\*  A. In the simplest terms, when you distribute anything containing VSCP & Friends code, you must make the source code to VSCP & Friends available under the terms of the GPL.





\*  Q. What if I make changes to VSCP & Friends or write new code based on VSCP & Friends code?



\*  A. Then you must make those changes available as well.





\*  Q. Do I have to distribute the source code to my application? Isn't the GPL “viral”?



\*  A. You do not have to distribute any code under the terms of the GPL other than VSCP & Friends code or code derived from VSCP & Friends. For example, if you write a port based on copying an existing VSCP & Friends in any way, you must make the source code available with the binary. However you would not need to make available any other code, such as the code of a wholly separate application linked with VSCP & Friends. 



\#\#\#\#\# Full GNU GPL License



This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or \(at your option\) any later version. 



This file is part of the VSCP \(\[http://can.sourceforge.net\]\) Copyright \(C\) 2000-2013 Ake Hedman, Grodans Paradis AB, \`&lt;\[akhe@grodansparadis.com\]&gt;\` 



GNU GENERAL PUBLIC LICENSE



Version 3, 29 June 2007



Copyright © 2007 Free Software Foundation, Inc. \`&lt;\[http://fsf.org/\]&gt;\`



Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed. 



Preamble



The GNU General Public License is a free, copyleft license for software and other kinds of works.



The licenses for most software and other practical works are designed to take away your freedom to share and change the works. By contrast, the GNU General Public License is intended to guarantee your freedom to share and change all versions of a program--to make sure it remains free software for all its users. We, the Free Software Foundation, use the GNU General Public License for most of our software; it applies also to any other work released this way by its authors. You can apply it to your programs, too.



When we speak of free software, we are referring to freedom, not price. Our General Public Licenses are designed to make sure that you have the freedom to distribute copies of free software \(and charge for them if you wish\), that you receive source code or can get it if you want it, that you can change the software or use pieces of it in new free programs, and that you know you can do these things.



To protect your rights, we need to prevent others from denying you these rights or asking you to surrender the rights. Therefore, you have certain responsibilities if you distribute copies of the software, or if you modify it: responsibilities to respect the freedom of others.



For example, if you distribute copies of such a program, whether gratis or for a fee, you must pass on to the recipients the same freedoms that you received. You must make sure that they, too, receive or can get the source code. And you must show them these terms so they know their rights.



Developers that use the GNU GPL protect your rights with two steps: \(1\) assert copyright on the software, and \(2\) offer you this License giving you legal permission to copy, distribute and/or modify it.



For the developer's and author's protection, the GPL clearly explains that there is no warranty for this free software. For both user's and author's sake, the GPL requires that modified versions be marked as changed, so that their problems will not be attributed erroneously to authors of previous versions.



Some devices are designed to deny users access to install or run modified versions of the software inside them, although the manufacturer can do so. This is fundamentally incompatible with the aim of protecting user's freedom to change the software. The systematic pattern of such abuse occurs in the area of products for individuals to use, which is precisely where it is most unacceptable. Therefore, we have designed this version of the GPL to prohibit the practice for those products. If such problems arise substantially in other domains, we stand ready to extend this provision to those domains in future versions of the GPL, as needed to protect the freedom of users.



Finally, every program is threatened constantly by software patents. States should not allow patents to restrict development and use of software on general-purpose computers, but in those that do, we wish to avoid the special danger that patents applied to a free program could make it effectively proprietary. To prevent this, the GPL assures that patents cannot be used to render the program non-free.



The precise terms and conditions for copying, distribution and modification follow. 



TERMS AND CONDITIONS 



0. Definitions.



“This License” refers to version 3 of the GNU General Public License.



“Copyright” also means copyright-like laws that apply to other kinds of works, such as semiconductor masks.



“The Program” refers to any copyrightable work licensed under this License. Each licensee is addressed as “you”. “Licensees” and “recipients” may be individuals or organizations.



To “modify” a work means to copy from or adapt all or part of the work in a fashion requiring copyright permission, other than the making of an exact copy. The resulting work is called a “modified version” of the earlier work or a work “based on” the earlier work.



A “covered work” means either the unmodified Program or a work based on the Program.



To “propagate” a work means to do anything with it that, without permission, would make you directly or secondarily liable for infringement under applicable copyright law, except executing it on a computer or modifying a private copy. Propagation includes copying, distribution \(with or without modification\), making available to the public, and in some countries other activities as well.



To “convey” a work means any kind of propagation that enables other parties to make or receive copies. Mere interaction with a user through a computer network, with no transfer of a copy, is not conveying.



An interactive user interface displays “Appropriate Legal Notices” to the extent that it includes a convenient and prominently visible feature that \(1\) displays an appropriate copyright notice, and \(2\) tells the user that there is no warranty for the work \(except to the extent that warranties are provided\), that licensees may convey the work under this License, and how to view a copy of this License. If the interface presents a list of user commands or options, such as a menu, a prominent item in the list meets this criterion. 



1. Source Code.



The “source code” for a work means the preferred form of the work for making modifications to it. “Object code” means any non-source form of a work.



A “Standard Interface” means an interface that either is an official standard defined by a recognized standards body, or, in the case of interfaces specified for a particular programming language, one that is widely used among developers working in that language.



The “System Libraries” of an executable work include anything, other than the work as a whole, that \(a\) is included in the normal form of packaging a Major Component, but which is not part of that Major Component, and \(b\) serves only to enable use of the work with that Major Component, or to implement a Standard Interface for which an implementation is available to the public in source code form. A “Major Component”, in this context, means a major essential component \(kernel, window system, and so on\) of the specific operating system \(if any\) on which the executable work runs, or a compiler used to produce the work, or an object code interpreter used to run it.



The “Corresponding Source” for a work in object code form means all the source code needed to generate, install, and \(for an executable work\) run the object code and to modify the work, including scripts to control those activities. However, it does not include the work's System Libraries, or general-purpose tools or generally available free programs which are used unmodified in performing those activities but which are not part of the work. For example, Corresponding Source includes interface definition files associated with source files for the work, and the source code for shared libraries and dynamically linked subprograms that the work is specifically designed to require, such as by intimate data communication or control flow between those subprograms and other parts of the work.



The Corresponding Source need not include anything that users can regenerate automatically from other parts of the Corresponding Source.



The Corresponding Source for a work in source code form is that same work. 



2. Basic Permissions.



All rights granted under this License are granted for the term of copyright on the Program, and are irrevocable provided the stated conditions are met. This License explicitly affirms your unlimited permission to run the unmodified Program. The output from running a covered work is covered by this License only if the output, given its content, constitutes a covered work. This License acknowledges your rights of fair use or other equivalent, as provided by copyright law.



You may make, run and propagate covered works that you do not convey, without conditions so long as your license otherwise remains in force. You may convey covered works to others for the sole purpose of having them make modifications exclusively for you, or provide you with facilities for running those works, provided that you comply with the terms of this License in conveying all material for which you do not control copyright. Those thus making or running the covered works for you must do so exclusively on your behalf, under your direction and control, on terms that prohibit them from making any copies of your copyrighted material outside their relationship with you.



Conveying under any other circumstances is permitted solely under the conditions stated below. Sub licensing is not allowed; section 10 makes it unnecessary. 



3. Protecting User's Legal Rights From Anti-Circumvention Law.



No covered work shall be deemed part of an effective technological measure under any applicable law fulfilling obligations under article 11 of the WIPO copyright treaty adopted on 20 December 1996, or similar laws prohibiting or restricting circumvention of such measures.



When you convey a covered work, you waive any legal power to forbid circumvention of technological measures to the extent such circumvention is effected by exercising rights under this License with respect to the covered work, and you disclaim any intention to limit operation or modification of the work as a means of enforcing, against the work's users, your or third parties legal rights to forbid circumvention of technological measures. 



4. Conveying Verbatim Copies.



You may convey verbatim copies of the Program's source code as you receive it, in any medium, provided that you conspicuously and appropriately publish on each copy an appropriate copyright notice; keep intact all notices stating that this License and any non-permissive terms added in accord with section 7 apply to the code; keep intact all notices of the absence of any warranty; and give all recipients a copy of this License along with the Program.



You may charge any price or no price for each copy that you convey, and you may offer support or warranty protection for a fee. 



5. Conveying Modified Source Versions.



You may convey a work based on the Program, or the modifications to produce it from the Program, in the form of source code under the terms of section 4, provided that you also meet all of these conditions:



• a\) The work must carry prominent notices stating that you modified it, and giving a relevant date. 



• b\) The work must carry prominent notices stating that it is released under this License and any conditions added under section 7. This requirement modifies the requirement in section 4 to “keep intact all notices”. 



• c\) You must license the entire work, as a whole, under this License to anyone who comes into possession of a copy. This License will therefore apply, along with any applicable section 7 additional terms, to the whole of the work, and all its parts, regardless of how they are packaged. This License gives no permission to license the work in any other way, but it does not invalidate such permission if you have separately received it. 



• d\) If the work has interactive user interfaces, each must display Appropriate Legal Notices; however, if the Program has interactive interfaces that do not display Appropriate Legal Notices, your work need not make them do so.



A compilation of a covered work with other separate and independent works, which are not by their nature extensions of the covered work, and which are not combined with it such as to form a larger program, in or on a volume of a storage or distribution medium, is called an “aggregate” if the compilation and its resulting copyright are not used to limit the access or legal rights of the compilation's users beyond what the individual works permit. Inclusion of a covered work in an aggregate does not cause this License to apply to the other parts of the aggregate. 



6. Conveying Non-Source Forms.



You may convey a covered work in object code form under the terms of sections 4 and 5, provided that you also convey the machine-readable Corresponding Source under the terms of this License, in one of these ways:



• a\) Convey the object code in, or embodied in, a physical product \(including a physical distribution medium\), accompanied by the Corresponding Source fixed on a durable physical medium customarily used for software interchange. 



• b\) Convey the object code in, or embodied in, a physical product \(including a physical distribution medium\), accompanied by a written offer, valid for at least three years and valid for as long as you offer spare parts or customer support for that product model, to give anyone who possesses the object code either \(1\) a copy of the Corresponding Source for all the software in the product that is covered by this License, on a durable physical medium customarily used for software interchange, for a price no more than your reasonable cost of physically performing this conveying of source, or \(2\) access to copy the Corresponding Source from a network server at no charge. 



• c\) Convey individual copies of the object code with a copy of the written offer to provide the Corresponding Source. This alternative is allowed only occasionally and non commercially, and only if you received the object code with such an offer, in accord with subsection 6b. 



• d\) Convey the object code by offering access from a designated place \(gratis or for a charge\), and offer equivalent access to the Corresponding Source in the same way through the same place at no further charge. You need not require recipients to copy the Corresponding Source along with the object code. If the place to copy the object code is a network server, the Corresponding Source may be on a different server \(operated by you or a third party\) that supports equivalent copying facilities, provided you maintain clear directions next to the object code saying where to find the Corresponding Source. Regardless of what server hosts the Corresponding Source, you remain obligated to ensure that it is available for as long as needed to satisfy these requirements. 



• e\) Convey the object code using peer-to-peer transmission, provided you inform other peers where the object code and Corresponding Source of the work are being offered to the general public at no charge under subsection 6d.



A separable portion of the object code, whose source code is excluded from the Corresponding Source as a System Library, need not be included in conveying the object code work.



A “User Product” is either \(1\) a “consumer product”, which means any tangible personal property which is normally used for personal, family, or household purposes, or \(2\) anything designed or sold for incorporation into a dwelling. In determining whether a product is a consumer product, doubtful cases shall be resolved in favor of coverage. For a particular product received by a particular user, “normally used” refers to a typical or common use of that class of product, regardless of the status of the particular user or of the way in which the particular user actually uses, or expects or is expected to use, the product. A product is a consumer product regardless of whether the product has substantial commercial, industrial or non-consumer uses, unless such uses represent the only significant mode of use of the product.



“Installation Information” for a User Product means any methods, procedures, authorization keys, or other information required to install and execute modified versions of a covered work in that User Product from a modified version of its Corresponding Source. The information must suffice to ensure that the continued functioning of the modified object code is in no case prevented or interfered with solely because modification has been made.



If you convey an object code work under this section in, or with, or specifically for use in, a User Product, and the conveying occurs as part of a transaction in which the right of possession and use of the User Product is transferred to the recipient in perpetuity or for a fixed term \(regardless of how the transaction is characterized\), the Corresponding Source conveyed under this section must be accompanied by the Installation Information. But this requirement does not apply if neither you nor any third party retains the ability to install modified object code on the User Product \(for example, the work has been installed in ROM\).



The requirement to provide Installation Information does not include a requirement to continue to provide support service, warranty, or updates for a work that has been modified or installed by the recipient, or for the User Product in which it has been modified or installed. Access to a network may be denied when the modification itself materially and adversely affects the operation of the network or violates the rules and protocols for communication across the network.



Corresponding Source conveyed, and Installation Information provided, in accord with this section must be in a format that is publicly documented \(and with an implementation available to the public in source code form\), and must require no special password or key for unpacking, reading or copying. 



7. Additional Terms.



“Additional permissions” are terms that supplement the terms of this License by making exceptions from one or more of its conditions. Additional permissions that are applicable to the entire Program shall be treated as though they were included in this License, to the extent that they are valid under applicable law. If additional permissions apply only to part of the Program, that part may be used separately under those permissions, but the entire Program remains governed by this License without regard to the additional permissions.



When you convey a copy of a covered work, you may at your option remove any additional permissions from that copy, or from any part of it. \(Additional permissions may be written to require their own removal in certain cases when you modify the work.\) You may place additional permissions on material, added by you to a covered work, for which you have or can give appropriate copyright permission.



Notwithstanding any other provision of this License, for material you add to a covered work, you may \(if authorized by the copyright holders of that material\) supplement the terms of this License with terms:



• a\) Disclaiming warranty or limiting liability differently from the terms of sections 15 and 16 of this License; or



• b\) Requiring preservation of specified reasonable legal notices or author attributions in that material or in the Appropriate Legal Notices displayed by works containing it; or



• c\) Prohibiting misrepresentation of the origin of that material, or requiring that modified versions of such material be marked in reasonable ways as different from the original version; or 



• d\) Limiting the use for publicity purposes of names of licensors or authors of the material; or 



• e\) Declining to grant rights under trademark law for use of some trade names, trademarks, or service marks; or 



• f\) Requiring indemnification of licensors and authors of that material by anyone who conveys the material \(or modified versions of it\) with contractual assumptions of liability to the recipient, for any liability that these contractual assumptions directly impose on those licensors and authors.



All other non-permissive additional terms are considered “further restrictions” within the meaning of section 10. If the Program as you received it, or any part of it, contains a notice stating that it is governed by this License along with a term that is a further restriction, you may remove that term. If a license document contains a further restriction but permits re licensing or conveying under this License, you may add to a covered work material governed by the terms of that license document, provided that the further restriction does not survive such re licensing or conveying.



If you add terms to a covered work in accord with this section, you must place, in the relevant source files, a statement of the additional terms that apply to those files, or a notice indicating where to find the applicable terms.



Additional terms, permissive or non-permissive, may be stated in the form of a separately written license, or stated as exceptions; the above requirements apply either way. 



8. Termination.



You may not propagate or modify a covered work except as expressly provided under this License. Any attempt otherwise to propagate or modify it is void, and will automatically terminate your rights under this License \(including any patent licenses granted under the third paragraph of section 11\).



However, if you cease all violation of this License, then your license from a particular copyright holder is reinstated \(a\) provisionally, unless and until the copyright holder explicitly and finally terminates your license, and \(b\) permanently, if the copyright holder fails to notify you of the violation by some reasonable means prior to 60 days after the cessation.



Moreover, your license from a particular copyright holder is reinstated permanently if the copyright holder notifies you of the violation by some reasonable means, this is the first time you have received notice of violation of this License \(for any work\) from that copyright holder, and you cure the violation prior to 30 days after your receipt of the notice.



Termination of your rights under this section does not terminate the licenses of parties who have received copies or rights from you under this License. If your rights have been terminated and not permanently reinstated, you do not qualify to receive new licenses for the same material under section 10.



9. Acceptance Not Required for Having Copies.



You are not required to accept this License in order to receive or run a copy of the Program. Ancillary propagation of a covered work occurring solely as a consequence of using peer-to-peer transmission to receive a copy likewise does not require acceptance. However, nothing other than this License grants you permission to propagate or modify any covered work. These actions infringe copyright if you do not accept this License. Therefore, by modifying or propagating a covered work, you indicate your acceptance of this License to do so. 



10. Automatic Licensing of Downstream Recipients.



Each time you convey a covered work, the recipient automatically receives a license from the original licensors, to run, modify and propagate that work, subject to this License. You are not responsible for enforcing compliance by third parties with this License.



An “entity transaction” is a transaction transferring control of an organization, or substantially all assets of one, or subdividing an organization, or merging organizations. If propagation of a covered work results from an entity transaction, each party to that transaction who receives a copy of the work also receives whatever licenses to the work the party's predecessor in interest had or could give under the previous paragraph, plus a right to possession of the Corresponding Source of the work from the predecessor in interest, if the predecessor has it or can get it with reasonable efforts.



You may not impose any further restrictions on the exercise of the rights granted or affirmed under this License. For example, you may not impose a license fee, royalty, or other charge for exercise of rights granted under this License, and you may not initiate litigation \(including a cross-claim or counterclaim in a lawsuit\) alleging that any patent claim is infringed by making, using, selling, offering for sale, or importing the Program or any portion of it. 



11. Patents.



A “contributor” is a copyright holder who authorizes use under this License of the Program or a work on which the Program is based. The work thus licensed is called the contributor's “contributor version”.



A contributor's “essential patent claims” are all patent claims owned or controlled by the contributor, whether already acquired or hereafter acquired, that would be infringed by some manner, permitted by this License, of making, using, or selling its contributor version, but do not include claims that would be infringed only as a consequence of further modification of the contributor version. For purposes of this definition, “control” includes the right to grant patent sub licenses in a manner consistent with the requirements of this License.



Each contributor grants you a non-exclusive, worldwide, royalty-free patent license under the contributor's essential patent claims, to make, use, sell, offer for sale, import and otherwise run, modify and propagate the contents of its contributor version.



In the following three paragraphs, a “patent license” is any express agreement or commitment, however denominated, not to enforce a patent \(such as an express permission to practice a patent or covenant not to sue for patent infringement\). To “grant” such a patent license to a party means to make such an agreement or commitment not to enforce a patent against the party.



If you convey a covered work, knowingly relying on a patent license, and the Corresponding Source of the work is not available for anyone to copy, free of charge and under the terms of this License, through a publicly available network server or other readily accessible means, then you must either \(1\) cause the Corresponding Source to be so available, or \(2\) arrange to deprive yourself of the benefit of the patent license for this particular work, or \(3\) arrange, in a manner consistent with the requirements of this License, to extend the patent license to downstream recipients. “Knowingly relying” means you have actual knowledge that, but for the patent license, your conveying the covered work in a country, or your recipient's use of the covered work in a country, would infringe one or more identifiable patents in that country that you have reason to believe are valid.



If, pursuant to or in connection with a single transaction or arrangement, you convey, or propagate by procuring conveyance of, a covered work, and grant a patent license to some of the parties receiving the covered work authorizing them to use, propagate, modify or convey a specific copy of the covered work, then the patent license you grant is automatically extended to all recipients of the covered work and works based on it.



A patent license is “discriminatory” if it does not include within the scope of its coverage, prohibits the exercise of, or is conditioned on the non-exercise of one or more of the rights that are specifically granted under this License. You may not convey a covered work if you are a party to an arrangement with a third party that is in the business of distributing software, under which you make payment to the third party based on the extent of your activity of conveying the work, and under which the third party grants, to any of the parties who would receive the covered work from you, a discriminatory patent license \(a\) in connection with copies of the covered work conveyed by you \(or copies made from those copies\), or \(b\) primarily for and in connection with specific products or compilations that contain the covered work, unless you entered into that arrangement, or that patent license was granted, prior to 28 March 2007.



Nothing in this License shall be construed as excluding or limiting any implied license or other defenses to infringement that may otherwise be available to you under applicable patent law. 



12. No Surrender of Others Freedom.



If conditions are imposed on you \(whether by court order, agreement or otherwise\) that contradict the conditions of this License, they do not excuse you from the conditions of this License. If you cannot convey a covered work so as to satisfy simultaneously your obligations under this License and any other pertinent obligations, then as a consequence you may not convey it at all. For example, if you agree to terms that obligate you to collect a royalty for further conveying from those to whom you convey the Program, the only way you could satisfy both those terms and this License would be to refrain entirely from conveying the Program.



13. Use with the GNU Affero General Public License.



Notwithstanding any other provision of this License, you have permission to link or combine any covered work with a work licensed under version 3 of the GNU Affero General Public License into a single combined work, and to convey the resulting work. The terms of this License will continue to apply to the part which is the covered work, but the special requirements of the GNU Affero General Public License, section 13, concerning interaction through a network will apply to the combination as such. 



14. Revised Versions of this License.



The Free Software Foundation may publish revised and/or new versions of the GNU General Public License from time to time. Such new versions will be similar in spirit to the present version, but may differ in detail to address new problems or concerns.



Each version is given a distinguishing version number. If the Program specifies that a certain numbered version of the GNU General Public License “or any later version” applies to it, you have the option of following the terms and conditions either of that numbered version or of any later version published by the Free Software Foundation. If the Program does not specify a version number of the GNU General Public License, you may choose any version ever published by the Free Software Foundation.



If the Program specifies that a proxy can decide which future versions of the GNU General Public License can be used, that proxy's public statement of acceptance of a version permanently authorizes you to choose that version for the Program.



Later license versions may give you additional or different permissions. However, no additional obligations are imposed on any author or copyright holder as a result of your choosing to follow a later version. 



15. Disclaimer of Warranty.



THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM “AS IS” WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION. 



16. Limitation of Liability.



IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR CONVEYS THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM \(INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS\), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES. 



17. Interpretation of Sections 15 and 16.



If the disclaimer of warranty and limitation of liability provided above cannot be given local legal effect according to their terms, reviewing courts shall apply local law that most closely approximates an absolute waiver of all civil liability in connection with the Program, unless a warranty or assumption of liability accompanies a copy of the Program in return for a fee.



END OF TERMS AND CONDITIONS





\#\# Where is the project located?



Current information about VSCP \(Very Simple Control Protocol\) can be found at:

\[http://www.vscp.org\]\(http://www.vscp.org\)



There is a forum/mailing lists available \[here\]\(https///groups.google.com/forum/\#!forum/vscp\) where you an ask for help or discuss VSCP development.





\#\# When was the project started?



Many of the thoughts behind this protocol come from work done by Ake Hedman as early as 1986 but the high node costs at the time made it impossible to do the things VSCP can do today. The official start date/time is \*\*2000-08-28 14:07 CET\*\* when the EDA project \[http://sourceforge.net/projects/eda\]\(http://sourceforge.net/projects/eda\) was registered at Sourceforge. EDA, is an acronym for \*\*Event-Decision-Action\*\* and is still preserved in the decision matrix of VSCP. 



\#\#  Why another protocol? 



VCSP is designed to be used where other solutions are to expensive to implement. This can typically be in code overhead where most other protocols use more resources \(flash/ram\) on a micro-controller than the actual “application” adding a lot of cost to the project. VSCP can work with a typical lowest cost dumb nodes like the Microchip MCP250xx series, to a 1K-2K flash micro controller module up to a full implementation with all features in about 5K flash. VSCP is both free and open. Everyone can join the project and help to add features and functionality to the protocol. There is free firmware and driver code available for most micro-controllers which uses many communication techniques. Everyone is free to use this code and there is not requirement to share any new code you develop, although most choose to, in order to improve the code base. 



\#\#  Why is the VSCP protocol needed? 



Most people don't remember the world looked like for PC developers before Windows where introduced. This was a time when the developer needed to ship a big bunch of floppy disks with his/hers application. One big pile of floppies where for different printers. Another set of disk was for different graphical cards and yet another for different pointing devices etc. It was not uncommon to have one floppy for the application an fifteen to twenty for drivers.



Windows changed this. The OS introduced abstraction for devices and from that point drivers was something the OS dealt with and the application developer could concentrate on creating the application. This was the big reason behind the boom in software that made Microsoft and others successful.



VSCP does this for automation tasks. Look around and see how it looks today. We have applications that work for Zigbee, X10, KNX, LonWorks etc. Some try to combine them into one application like MrHouse and the like but still it's a different thing to turn on a lamp using Zigbee, X10, KNX or whatever. In the best case the same user interface component can be used but still there is a need to differentiate between the technologies use also at that level and most important the knowledge about the technology is needed on the top level.



VSCP try to hide this. Drivers implement the interface to the technology and they all talk to the system using the VSCP protocol and understand VSCP protocol events. Compare this with printing under a modern OS. It's no difference today if you print to a Laser printer or a ink jet printer. Also it all works the same if the printer use protocol x, y or z. You are also still able to configure and print with the printers. This is where the abstraction comes into place.



To switch on a lamp \(or a group of lamps\) in VSCP we send a



    CLASS1.CONTROL, Type=5, TurnOn event.



A driver translate this event to its own format and does its specific work using its own protocol and return a



    CLASS1.INFORMATION, Type=3, ON event 



When its job is done as a confirmation for the rest of the system.



An application does not need to bother how the actual control is done. On the application level it's enough to implement a button and some visual indication to indicate the outcome of the operation.



A system to present some measurement data is another example. Think of a system with temperature sensors. They all use different technologies but a driver for each translate the temperature readings to a common



    CLASS1.MEASUREMENT, Type=6, Temperature measurement events. 



This event is region independent and format independent. It is easy to create a driver that log this value into a database. Also here in a common format. You can now build a web applet that shows the temperature for every possible temperature sensor. As the format is common and easy to collect in a database in a common way you can also write a statistical application that show temperature data and work for any temperature sensor.



The above is the most important reason for VSCP but there is more.



Each VSCP device have a common way it can be configured by. This means one high level software can be used for all devices. Note that a device necessarily does not need to implement this. Instead a driver can do that and make it look like a VSCP device. Typically is a 1-wire sensor where the driver can implement the parameters for it and export it in a common way.



All VSCP devices are described in a common way. The device itself holds this information and therefore when a device is found all information about how it is configured and used is available. Again this information can be implemented in the driver.



VSCP defines a lot more functionality and can be used all the way out to the actual device. Still the most important part is the abstraction. 



\#\# How does it work?



\#\#\# Events



VSCP is an event based system. Nodes generate events and nodes react on events. Normally events are not addressed but instead are broadcast on the bus. Its up to the receiving end to decide if its interested in the event or not. All events have an originating address for the node they are sent from. This is a GUID consisting of 16 bytes but a shorter, typically, one byte nickname-ID is used on most system. It is always possible to deduce the full GUID from the nickname. Events are divided into groups. First there is Level I and Level II events. Level I events are limited to a maximum of eight bytes of data while Level II events can have up to 488 bytes of data. The low maximum data count for Level I comes from that CAN has been used as the least common denominator. This does not limit VSCP Level I to be used only over CAN. Both Level I and Level II events are divided into a class and a type. The class defines a group of events of a specific type. Typical examples are classes for measurements, information and control. As mentioned above events are not addressed. This is not entirely true as one class in each level \(CLASS1.PROTOCOL and CLASS2.PROTOCOL\) have events that are addressed. These classes define protocol functionality that all nodes have to implement. Typical examples found there are event types for boot loader, register access and status information. Most of the events can use a zone/sub-zone to identify the group of nodes it is relevant to.



\#\#\# Registers



Each node has a specified number of byte wide registers defined. This is the second interface to the black box the node represents. The register space of a node is 256 bytes divided in two halves. The lower part \(0x00-0x7F\) is application specific. The upper part content is mandatory and specified by VSCP. This space hold, among many other things, the firmware and hardware version of the node. The GUID, user module id, alarm status and similar registers. In the top of the mandatory register space is a 32 byte string stored, the MDF, which contains an URL that points to a location where to find an XML file that describe this module its registers and its functionality. The lower part of the register space is used to define control and status registers and more complex structures. The area is mapped and 65535 pages can be used if needed allowing for very complex scenarios if needed.



\#\#\# MDF - Module Description File



The MDF file describe the module at a high level. It provides information about the manufacturer of the module, the events that can be expected from it and the definition of its register content. The MDF looks at the module from a high level perspective and can see floating point values, bit arrays, option tables in register space and thus give application software a way to present registers in a much more user friendly way. There is two way to obtain the MDF after getting it from the module by reading the registers holding it . As VSCP is designed for low end nodes it is normally to much for such a node to have the MDF stored internally. In this case the string points to a web server from which the XML can be downloaded and processed. In a more capable module with more resources the MDF is stored internally in which case the read string has zero length and in this case the MDF data can be fetched from the module itself. The node constructor decide which method he/she wants to use. The MDF also point out where drivers for different environments and systems for the module and user manuals etc can be found.



\#\#\# DM - Decision Matrix



All nodes can optionally implement a decision matrix. This matrix is used to define one or a group of events that should trigger a predefined functionality at the module. In VSCP this is called the Event-Decision-Action mechanism from the predecessor of the project which was called EDA. A typical examples can be to trigger a relay. The module got one action that set the relay and another action that reset it. Typically this could be implemented hard coded so that the relay would be set when an ON-event was received and has been reset when an OFF-event was received. With the use of the DM it is easy to use any event to trigger the action not just the ON/OFF events. Physically the DM is located in register space just as any other parameters of the module so register access functions are used to changed it.



\#\#\# Measurements



A special class is used for measurements and events for all SI units and derived units is defined. The class will grow over time when new types are needed. This means that for example a temperature measurement is normally sent as a Kelvin temperature. Celsius and Fahrenheit is also possible in this case and similar alternatives is available for other types but the SI unit is always the default. How the measurement is presented in the frame is also well specified. Bit field, string, integer, normalized integer \(decimal\) and floating point values are possible. The normalized integer is especially well suited for a low end system to send decimal data. As the event and its content is well specified it is very easy to interpret the data on the receiving end where it should be processed, stored in a database, logged or displayed.



\#\#\# Putting it all together



As VSCP is event based, one often need to think a bit differently when constructing a system. A typical example is a tank with a level sensor and a pump which together construct a self contained system. A traditional system system would have used a master to control the pump and the sensor. In VSCP we allow for this also but try to distribute as much of the intelligence as possible to the nodes themselves. So what we do is to tell the level sensor to send level information with a predefined interval. Several sensors can be added for redundancy. We tell the pump that it should start to fill up the tank when the tank reach a low level and stop at a high level. This might be dangerous as the sensor may stop working, the cable get cut or whatever. In this case the we also program the pump goes to its safe state == pump off and alarming this state to the rest of the system when it does not receive sensor measurements any more.. This “safe state“ is often possible to find for most control situations. As the transport mechanism is unknown to the application, timing must be very lose for VSCP. We cannot be certain when an event arrives or if it arrives. Many transport mechanisms, such as CAN and TCP/IP, makes delivery more certain while other solutions like UDP, RF and PLC can be problematic. It is therefore very important that a sent event always get a confirmation event back. For some nodes this might not be important. A temperature node or the level sensor node above just send there measurements and don't care if someone uses them or not. This thinking is central. The node that originate an event should – if possible - know as little as possible about how the event it sends out will be used. This make the system very flexible. 



\#\#\# The "Friends"



A software package called VSCP & Friends is available to support VSCP users. This package can be downloaded and used for free and contain a lot of application and code. Everything is available both for Windows and Linux based systems.



First and possibly most important it contain the VSCP daemon. This is a server software that makes it possible to control several VSCP segments over the Internet. 



The server expose a secure Internet interface and makes it possible to add drivers for segments of nodes or special equipment. A driver can communicate with the server using the CANAL interface for a Level I driver and the TCP/IP interface for a Level II driver. 



CANAL stands for CAN Abstraction Layer and was initially developed as a software layer between application software and CAN equipment. For the VSCP it is not limited to interface CAN equipment but CAN drivers for most CAN adapters such as PEAK, IXXAT, PORT etc is included in the package as many CAN users use the system.



A lot of code is available that confirms to the CANAL interface. This same code can be used to communicate directly to a device that use the CANAL driver as can be used to talk to the daemon. This makes, among many other advantages, it easy to build simulated systems that use the same code base as the resulting system.



The daemon can do a lot more such as remotely replace/install drivers, remotely handle users and permissions, set up and handle an internal decision matrix to set up a self contained control system etc.



VSCP Works is a client application that is included in the package. This application can be used to send/receive VSCP events to/from every segment/device that export a CANAL interface and also talk to a remote VSCP daemon. VSCP Works can be used to investigate register space on any VSCP node and will also have support for remote firmware upgrade. 



Server and client application is released under the GPL license. Libraries and classes is released under a modified LGPL license that make sure they can be used in proprietary projects.



Maybe the most important aspect of the VSCP & Friends package is that it can be used as an abstraction for interfacing other technologies and protocols. One just need to build a driver that translate the systems functionality to/from VSCP events and then install this driver for the VSCP daemon and then remote control functionality, software interface etc is directly available. This way one application interface can be constructed to control several technologies using different protocols. One can compare this to the situation for printers before windows was announced. Each application needed to distribute a stack of disks with printer drivers. Windows ended this by introducing the printer API abstraction for printers. VSCP & Friends does the same for SECO \(SEensor/COntrol\) devices .



A web interface named OHAS is under development that will make it possible to build dynamic control interfaces with drag and drop technology. 



\#\#\# Summary



VSCP makes it easy and very cost effective to build systems with distributed intelligence. The protocol is placed in the Public Domain so it is therefore free for anyone to use and modify to their own needs. VSCP can be used all the way from the application down to the device but it can also be used as an abstraction to other technologies so one application can be written that transparently use several different technologies..



More information and downloads is available at \[http://www.vscp.org\]\(http://www.vscp.org\)



\\ 

----

{{  ::copyright.png?400  \|}}



\`&lt;HTML&gt;\`\`&lt;p style="color:red;text-align:center;"&gt;\`\`&lt;a href="http://www.paradiseofthefrog.com"&gt;\`Paradise of the Frog AB\`&lt;/a&gt;\`\`&lt;/p&gt;\`\`&lt;/HTML&gt;\`

