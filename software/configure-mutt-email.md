# Install & Configure Mutt Email (Gmail Account)

### Gmail
* Generate [app password](https://support.google.com/accounts/answer/185833) for gmail

### Install Mutt
```bash
sudo apt-get install mutt
```

### Configure Mutt
* Create Configuration Files

```bash
mkdir -p ~/.mutt/cache/headers
```

```bash
mkdir ~/.mutt/cache/bodies
```

```bash
touch ~/.mutt/certificates
```

```bash
touch ~/.mutt/muttrc # Configuration file
```

* Edit Configuration File

```bash
vim ~/.mutt/muttrc
```

* Add Configuration
```bash
set ssl_starttls=yes
set ssl_force_tls=yes

set imap_user = "EMAIL"
set imap_pass = "PASSWORD"

set from="EMAIL"
set realname="Your Name"

set folder = "imaps://imap.gmail.com/"
set spoolfile = "imaps://imap.gmail.com/INBOX"
set postponed="imaps://imap.gmail.com/[Gmail]/Drafts"

set header_cache = "~/.mutt/cache/headers"
set message_cachedir = "~/.mutt/cache/bodies"
set certificate_file = "~/.mutt/certificates"

set smtp_url = "smtps://EMAIL:PASSWORD@smtp.gmail.com:465/"

set move = no
set imap_keepalive = 900
```
