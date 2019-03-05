## FREQUENTLY ASKED QUESTIONS

**Where is all the my servers and sites information/ metadata
    saved?**

Cleaver doesn't save any of your information in the cloud. This
    means you own the information about your servers and sites and
    nobody else. They are saved on your local machine in a single file -
   `cleaver.db`. The location depends on the type of Operating
    System you are using:

 On OSX: `~/Library/Application Support/cleaver/`

 On Windows:  `%APPDATA%/cleaver`

 On Linux:   `$XDG_CONFIG_HOME/cleaver` or `~/.config/cleaver`

**What are the steps for creating and provisioning a DigitalOcean server?**

* Please follow [these steps][provisioning].


**What are the steps for creating and provisioning a Vultr server?**

* Please follow [these steps][provisioning].

**What does Cleaver do to my server when provisioning? What software gets installed?**
  * Following are some of the important operations that Cleaver performs when provisioning your server:
    - Installs Ubuntu 18.04 and some packages - `wget`, `unzip`, and `zip`
    - Configures automatic security updates
    - Creates a swap file
    - Creates a non-admin user named `cleaver`
    - Adds public keys of GitHub, GitLab, and BitBucket to make it easy to deploy your web apps
    - Configures SSH and disabled password authentication
    - Configures firewall that allows SSH connection on Port 22, TCP connections on both port 80 and 443
    - Configures fail2ban
    - Installs and configures supervisor
    - Installs and configures Nginx

[provisioning]: /servers/provisioning.md
