## SITES
---

Creating secure sites with Cleaver only takes few easy steps. Cleaver try to automate things as much as possible for you so that you could focus your time on doing things what you are good at - crafting beautiful and useful web apps.

Among few other complex things, Cleaver takes care of adding domain records, installing missing dependencies, installing SSL certificates with auto-renewal on, ensuring proper files and folders permissions, configuring PHP-FPM (where applicable), configuring nginx, creating log files, setting up site to make it easy for zero downtime deployments and few more! We told you, Cleaver saves you hours of your valuable time.

### Adding Domain

When you add a (sub)domain, Cleaver will automatically add an `A record` for the domain to the cloud provider if it does not exist already. While creating an A record, Cleaver also adds an `A record` for `www` subdomain. What this means is that, after adding a site, say example.com, it will be accessible using both www.example.com and example.com. There is no extra step to add a domain; you add a domain when creating a site.