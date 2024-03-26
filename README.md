### Description

This setup is based on [OpenSMTPD](https://opensmtpd.org/), [Dovecot](https://www.dovecot.org/) and [Rspamd](https://www.rspamd.com/).

OpenSTMPD and the other software required by this installation runs on everything.
At the [link section](#links) you'll find step by step instructions for FreeBSD, Linux and OpenBSD.

This repo is intended to be OS independent, so in conf directory you'll find the very basic config of OpenSMTPD, Dovecot and rspamd.
Mind that path to config files varies from OS to OS and even within different distros of Linux.
I found useful to create /etc/mail directory in any case to have specific files like aliases and users inside it.

This is very simple setup without sql backend for example though you can easily do so.
OpenSMTPD supports sqlite.

### Prerequisites

This setup supposes that you have required DNS records and all needed packages installed.
[This filter](https://github.com/poolpOrg/filter-rspamd) is used for integrating Rspamd with OpenSMTPD.
You can install it from packages on BSD systems or compile it from source on Linux.
You also have to add vmail user in your system.

### Links

The articles listed below are very handy when you setup mail server of this kind.
PDF with these articles are saved to PDF dir at this repo.
But first of all if you want to get deep understanding of OpenSTMPD - the heart of this setup -
take a look at:

[OpenSMTPD Book](https://github.com/poolpOrg/OpenSMTPD-book)

written by one of the main authors of OpenSMTPD, who is also running blog at

https://poolp.org

where you can find many other useful materials and news about OpenSMTPD.

- https://www.davd.io/posts/2021-12-18-freebsd-mail-server-part-1/

- https://coderwall.com/p/eejzja/simple-smtp-server-with-opensmtpd

- https://www.tumfatig.net/2023/self-hosted-email-services-on-openbsd/

- https://prefetch.eu/blog/2020/email-server/

- https://prefetch.eu/blog/2020/email-server-extras/

- https://prefetch.eu/blog/2022/email-server-revisited/

- https://github.com/poolpOrg/poolp.org/blob/master/content/posts/2019-09-14/index.md
