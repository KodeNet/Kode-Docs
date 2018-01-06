---
title: BitlBee
taxonomy:
    category:
        - docs
---

> BitlBee brings IM (instant messaging) to IRC clients and supports multiple IM networks/protocols including XMPP/Jabber.

## Connecting
BitlBee users can connect a KodeNet Jabber ID using a preferred IRC (Internet Relay Chat) client. The described steps use the irssi client, but the same commands apply to any other IRC clients. With BitlBee it looks like you're connecting to an IRC server, only you're not. Instead, BitlBee will only be listening on localhost and the standard IRC port 6667.

#### Add Account
`account add <protocol> <username> [<password>]`

###### Example 
`account add jabber demo@kode.im demopassword`

![BitlBee](/user/pages/media/bitlbee/connect/step1.png)

#### Enable Account
`account [<account id>] on`

###### Example
`account demo@kode.im on`

The XMPP/Jabber account should now show a successful connection with 
```
jabber - Logging in: Connected to server, logging in
jabber - Logging in: Authentication finished
jabber - Logging in: Authenticated, requesting buddy list
jabber - Logging in: Logged in
```
![BitlBee](/user/pages/media/bitlbee/connect/step2.png)

#### Display Roster/BuddyList

`blist [all|online|offline|away] [<pattern>]`

###### Example
`blist all`
![BitlBee](/user/pages/media/bitlbee/connect/step3.png)

>>>>> By default newly connected accounts will see a **Support** contact join the roster list. This contact is not required to have and can be removed or re-added at anytime. This contact is simply available for questions and assistance.

#### Resources
+ [Official BitlBee User Guide](https://www.bitlbee.org/user-guide.html)
+ [Official BitlBee Wiki](https://wiki.bitlbee.org)
