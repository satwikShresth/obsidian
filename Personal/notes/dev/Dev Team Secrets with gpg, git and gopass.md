---
title: "Dev Team Secrets with gpg, git and gopass"
source: "https://www.youtube.com/watch?v=EB9cW9RjiSs"
author:
  - "[[Andrew Tropin]]"
published: 2020-05-20
created: 2025-08-28
description: "#Japan #USA #Trade #PrashantDhawan #PrashantSirUse Code 𝐏𝐃𝟏𝟎 to get the Maximum Discount on our Course- 𝐁𝐚𝐭𝐜𝐡 𝐒𝐭𝐚𝐫𝐭𝐢𝐧𝐠 𝐨𝐧 𝟑𝟎 𝐀𝐮𝐠𝐮𝐬?..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=EB9cW9RjiSs)  

How to manage credentials/secrets for development team, how to store and share production environment configs and  
  
Our today guest:  
Andrew Zhurov  
https://github.com/andrewzhurov

##notes


- Once the store is initialized we can store the whole file directly as a .env

To setup for other side of the screen we need 

gpg, git and gopass

The process

- Initalize gpg key for yourself

```bash
gpg --gen-key
# add name, email, passphrase
```

- Initalize root password store using gopass

```bash
gopass init
```

- Clone repo

```bash
gopass clone <git-repo> <store-name> #In our case will be secrets
```

- Sync 

```bash
gopass sync
```

- Add yourself as recipient

```bash
gopass recipients add
```

Then I will go ahead add all the new recipients to allow everyone to access the keys