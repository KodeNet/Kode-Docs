---
title: Profanity
taxonomy:
    category:
        - docs
metadata:
    'og:title': Profanity
    'og:description': Use the Profanity console client to get connected to the KodeNet XMPP/Jabber network.
    'og:url': https://www.koderoot.net/docs/desktop/profanity
    'og:image': http://www.profanity.im/images/profanity_logo.png
---

> Profanity is a text mode instant messaging interface that supports the XMPP protocol and runs on Linux, macOS and Windows using Cygwin.

## Connecting
The Profanity user guide covers many topics in detail. These steps can be used to get quickly connected to your KodeNet account.

```
/account add default
/account set default jid user@kode.im
/account set default password  ...
/autoconnect set default
/connect default
```

>>>>> By default newly connected accounts will see a **Support** contact in the roster list. This contact is not required to have and can be removed or re-added at anytime. This contact is simply available for questions and assistance.

### Group Chat
Joining a group chat with Profanity is simple. For example, to join the **kodenet** group chat simply use the `/join` command.

`/join kodenet@muc.kode.im`

![Profanity](/user/pages/media/profanity/Profanity.png)

#### Resources
+ [Profanity User Guide](http://www.profanity.im/userguide.html)
+ [GitHub](https://github.com/boothj5/profanity)
+ [OMEMO](https://github.com/ReneVolution/profanity-omemo-plugin)
