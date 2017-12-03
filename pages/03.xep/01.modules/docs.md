---
title: 'XMPP Modules'
taxonomy:
    category:
        - docs
---

## Intro
>The core specifications for XMPP are developed at the Internet Engineering Task Force (IETF) - see [RFC 6120](https://datatracker.ietf.org/doc/rfc6120/), [RFC 6121](https://datatracker.ietf.org/doc/rfc6121/), and [RFC 7622](https://datatracker.ietf.org/doc/rfc7622/) (along with a WebSocket binding defined in [RFC 7395](https://datatracker.ietf.org/doc/rfc7395/))

Prosody - the service powering KodeNet XMPP/Jabber communication services is customized to use _modules_, synonymous to _plugins_ to add features and functionality. These modules are defined by their respected XMPP specification. We will be highlighting some of the more common modules that are loaded and available for KodeNet XMPP users.

## Modules

#### [XEP-0191](https://xmpp.org/extensions/xep-0191.html): blocking
Simple Communications Blocking support.

#### [undefined]: block_strangers
This module blocks strangers not in your roster (also known as a Contact/Buddy List).

#### [XEP-0124](https://xmpp.org/extensions/xep-0124.html): bosh
Enable BOSH clients, also known as "Jabber over HTTP".

#### [XEP-0280](https://xmpp.org/extensions/xep-0280.html): carbons
Message Carbons allows users to maintain a shared and synchronized view of all conversations across all their online clients and devices.

#### [XEP-3057](https://xmpp.org/extensions/xep-0357.html): cloud_notify
The purpose of push notifications is to inform users of new messages or other pertinent information even when they have no XMPP clients online. Notifications are typically delivered to a user's mobile device.

#### [XEP-0352](http://xmpp.org/extensions/xep-0352.html): csi
This module implements Client State Indication, a way for mobile clients to tell the server that they are sitting in someones pocket and would rather not get some less urgent things pushed to it. Client State Indication works in conjunction with the following additional modules:

##### _throttle presence_ #####
This module works with csi to supress presence updates (Available, Away, Busy, etc).

##### _filter chatstates_ ##### 
This module also works with csi to remove chat states (Someone is typing…).

#### [XEP-0220](https://xmpp.org/extensions/xep-0220.html): dialback
This module is used between XMPP servers to provide identity verification. Server Dialback uses the Domain Name System (DNS) as the basis for verifying identity; the basic approach is that when a receiving server accepts a server-to-server connection from an initiating server, it does not process XMPP stanzas over the connection until it has verified the initiating server's identity.

#### [XEP-0030](https://xmpp.org/extensions/xep-0030.html): disco
With this module clients can discover services and features available on the server. Some clients will automatically take advantage of the available items while others will need manual configuration.

#### [undefined]: invite
This module allows users with an account to generate single-use invite URLs using an ad-hoc command. After the account is created, the inviter and the invitee are automatically added to the other’s roster. The inviter of a user is stored, so can be used later (for example, for detecting spammers).

#### [XEP-0313](https://xmpp.org/extensions/xep-0313.html): mam
Message Archive Management will archive all messages that match the simple rules setup by the user, and allow the user to access this archive.

#### [XEP-0136](http://xmpp.org/extensions/xep-0136.html): mam_archive
Because XEP-0136 defines a ‘conversation’ concept not present in XEP-0313, we have to assume some periods of chat history as ‘conversations’. Conversation interval defaults to one day, to provide for a convenient usage.

#### [XEP-0045](https://xmpp.org/extensions/xep-0045.html): muc
The Multi-User Chat specification defines an XMPP protocol extension for multi-user text chat, whereby multiple XMPP users can exchange messages in the context of a room or channel, similar to Internet Relay Chat (IRC).

#### [XEP-0163](https://xmpp.org/extensions/xep-0163.html): pep
Enables users to publish their mood, activity, playing music and more.

#### [XEP-0084](https://xmpp.org/extensions/xep-0084.html) & [XEP-0153](https://xmpp.org/extensions/xep-0153.html): pep_vcard_avatar 
This module pushes the users nickname and avatar from vCards into PEP, or into vCards from PEP. This allows interop between older clients that use XEP-0153: vCard-Based Avatars to see the avatars of clients that use XEP-0084: User Avatar and vice versa.

#### [XEP-0016](https://xmpp.org/extensions/xep-0016.html): privacy_lists
This specification defines an XMPP protocol extension for enabling or disabling communication with other entities on a network. This module is being phased out in favour of the newer simpler blocking (XEP-0191) protocol.

#### [XEP-0049](https://xmpp.org/extensions/xep-0049.html): private
Some clients offer users the ability to store arbitrary notes or client specific information on the server such as chatroom bookmarks which Prosody supports via mod_private (for room bookmarks, etc).

#### [XEP-0077](https://xmpp.org/extensions/xep-0077.html): register
This module allows users to register new accounts and change passwords. User passwords can be changed even if new user registration is disabled.

#### [XEP-0321](https://xmpp.org/extensions/xep-0321.html): remote_roster
This module adds support for Remote Roster Management which is commonly used to allow components such as transports to modify the rosters of local users.

#### [RFC-6121](https://xmpp.org/rfcs/rfc6121.html): roster
Any modifications made by a user to their roster is shared between all clients but some clients may need to log out and back in or manually request the updated roster before the changes are displayed. Rosters can also include user-defined groups.

#### [XEP-0199](https://xmpp.org/extensions/xep-0199.html): s2s_keepalive
This module periodically sends XEP-0199 ping requests to remote servers to keep your connection alive.

#### [XEP-0157](https://xmpp.org/extensions/xep-0157.html): server_contact_info
With this module various types of contact addresses are set (abuse, staff, feedback, security, contact). 

#### [XEP-0198](https://xmpp.org/extensions/xep-0198.html): smacks
This module provides reliability and fast reconnects for XMPP. By default XMPP is as reliable as your network is. Unfortunately in some cases that is not very reliable - in some network conditions disconnects can be frequent and message loss can occur. This is where the smacks module comes in. 

#### [XEP-0377](https://xmpp.org/extensions/xep-0377.html): spam_reporting
When someone reports spam or abuse, a line about this is logged and an event is fired so that other modules can act on the report.

#### [undefined]: support_contact
This module adds a default contact to newly registered accounts. The support or staff contact can be removed and re-added at any time.

#### [XEP-0202](http://xmpp.org/extensions/xep-0202.html) & [XEP-0090](http://xmpp.org/extensions/xep-0090.html): time
The time module implements XEP-0202 and the obsolete XEP-0090 for compatibility with older clients. This module lets others know the time here on the KodeNet XMPP servers.

#### [RFC-6120](https://xmpp.org/rfcs/rfc6120.html#tls): tls
This module adds support for secure TLS (Transport Layer Security) encryption on connected streams. By default TLS on KodeNet XMPP is required between client-to-client and server-to-server connections.

#### [XEP-0012](https://xmpp.org/extensions/xep-0012.html): uptime
This module allows the server to respond to requests for how long it has been running.

#### [XEP-0092](http://xmpp.org/extensions/xep-0092.html): version
Using this module allows the servers to respond to software version requests.

#### [XEP-0054](http://xmpp.org/extensions/xep-0054.html): vcard
This module allow users to set vCards containing contact information. Users are not required to fill in a vCard and can supply as much or as little as they like.

#### [undefined]: webpresence
Quite often you may want to publish your Jabber status to your blog or website. The webpresence module allows you to do exactly this. <img src="https://im.koderoot.net/status/staff" alt="online xmpp status" />

#### [RFC-7395](https://tools.ietf.org/html/rfc7395): websocket
WebSockets is a protocol for providing web pages with simple two-way communication with a web server. This module allows browsers to communicate with Prosody via XMPP over WebSockets. This usually induces less overhead than using BOSH.