---
description: Minimum security tips for all SPOs to follow.
---

# Security tips for SPOs.

_`Remember, this is the minimum, you cant go wrong with doing more if you wish to.`_

1. Use a hardware wallet for your pledge. See my guide at: [https://poolguide.frcan.com/readme-1](https://poolguide.frcan.com/readme-1)
2. Keep a few copies of your stake pool op keys offline and only in safe places.
3. Use air-gapped machine for all transactions signing.
4. Keeping the system updated is vital before starting anything on your system. This will prevent people to use known vulnerabilities to enter in your system:

```text
sudo apt-get update
sudo apt-get upgrade
sudo apt-get autoremove
sudo apt-get autoclean
```

   Enable automatic updates can be crucial for your server security. It is very important to stay up to date:

```text
sudo apt-get install unattended-upgrades
sudo dpkg-reconfigure -plow unattended-upgrades
```

To enable ONLY security updates, do this:

```text
sudo nano /etc/apt/apt.conf.d/50unattended-upgrades
```

Edit to look like this: 

> ```text
> : Unattended-Upgrade::Allowed-Origins {
> :     "${distro_id}:${distro_codename}-security";
> : //  "${distro_id}:${distro_codename}-updates";
> : //  "${distro_id}:${distro_codename}-proposed";
> : //  "${distro_id}:${distro_codename}-backports";
> : };
> : // Unattended-Upgrade::Mail "my_user@my_domain.com";
> ```

5. perfect your firewall settings: 





