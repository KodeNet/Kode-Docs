---
title: Info
taxonomy:
    category:
        - docs
--- 
#### Irssi
After launching Irssi execute the following command to connect securely to the KodeNet IRC network.

`/server add -auto -tls -tls_verify -network kodenet -port 6697 irc.koderoot.net`

Verify these settings are reflected in your Irssi config.

#### WeeChat 
Before connecting with WeeChat you must first specify the path of the Common CA certificates.

**Linux**
`/set weechat.network.gnutls_ca_file "/etc/ssl/certs/ca-certificates.crt"`

**macOS**
`/set weechat.network.gnutls_ca_file "/usr/local/etc/openssl/cert.pem"`

#### NickServ
Register a username.

>>>Note that new requests require email confirmation. 

`/msg nickserv register password email`


#### ChanServ
Register a channel.

`/msg chanserv register channel [description]`

#### HostServ
Request a virtual host so you can have something like `me@my.cool.vhost` or some other variation.

`/msg hostserv request vhost`

#### Client Certificates (optional)
```
openssl req -newkey rsa:2048 -days 3650 -x509 -keyout kodenet.key -out kodenet.crt -nodes
cat kodenet.crt kodenet.key > ~/.irssi/ssl/kodenet.pem
chmod 600 ~/.irssi/ssl/kodenet.pem
rm kodenet.crt kodenet.key
```

##### TLS cetificate fingerprint

`openssl x509 -sha1 -fingerprint -noout -in ~/.irssi/ssl/kodenet.pem | sed -e 's/^.*=//;s/://g;y/ABCDEF/abcdef/'`


