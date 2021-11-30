# Hodge-podge topics

Thursday = stegonography + final exam review

## Network Forensics

Allot more about AD policy, preventative stuff (logging attacks, performing forensics after the fact)

defn - a methodology to log and analyze traffic over networks

Lots of ransomware attacks. Happen all the time, high-profile targets sometime

Really easy way to make money for bad actors

Goal - how can we stop it from happening again? Use forensics to figure out what happened...

Can directly collect the traffic - the actual packages themselves.

Networks with over 100k people - UAB for example.

Full network logs - collected at ingress/egress devices. aka edge devices. normally firewalls.

Need to be prepared to capture data ahead of tiem. session data, metadata, from, to, what protocols

Statefullness - ability to detect protocol w/o the port - is important. Need to have enough computational
capability to capture session data, what protocol (actual, not just the port).

If your policy is good enough, you can trigger full packet captures for specific supsicious things. May
miss the start of the attack, but you get the majority of it.

Need to maintain uptime when conducting network forensics. 

## Email Forensics

Scams & phishing are big. Can't stop, just try to lessen the blow. Prey on ignorance, greed, desparation.

Need policies to regulate what is allowed to come in. User education.

Lots of information in SMTP headers. Some stuff can be spoofed. Pathway is nearly impossible to manipulate.
Message ID (if it's not there be suspicious). Message ID can lead you to a log in a mail server somewhere.

Attachments are a big vehicle for viruses. Base64. MIME encoding.

Understand how mail tools store messages. DBX in Windows. JSON, XML. used to be straight text. 
Tools to help with this.

Mail can be used by malicious users to commit crimes. Content is important here. 
Or it can be used by malicous users to attack people. Metadata is important here.

## Mobile Device Forensics

Cell phones communicate via towers. Log certain towers from pinging. With 2 towers, get a rough 
location, 3, get exact location.

Pivotal case (hugh's case) in MS. Defense: she wasn't there. What breaked the case was 
that she went back and called the guy. Towers triangulated that she was there at the time.

Scott Peterson - killer. Triangulated phone activity in the neighborhood.

Data - phone, text, web traffic, pictures (geolocation), calendars, voice recordings, social media.

Capturing data off of a phone. Put it in a Farraday bag/cage. Charge it since the battery is drained quickly
when it's isolated from cell signal. If it's on, leave it on. Collect on the peripheral.

Looking at the storage on the phone is important. 

Critical areas of storage:
1. Internal Memoroy
1. SIM Card
1. External Memory (SD Cards)
1. System Server (phone carrier's server) - voice mails, call logs, tower pings for traingulation

Apple encrypts devices - couldn't get into San Bernadino killer device

BTS - Basic Transciever Station (cell tower)

BSC - Case Sation Controller  - Management of towers

MSC - Mobile switching center. Server/db where logs are.

Other nations have other networks. Govt/military use other networks.

BUT they all use this same layout

Warrant - I want this ID for this range of time. Get a map of where you've been.

