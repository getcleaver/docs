## Adding Domain
---

When you add a (sub)domain, Cleaver will automatically add an `A record` for the domain to DigitalOcean if it does not exist already. While creating an A record, Cleaver also adds an `A record` for `www` subdomain. What this means is that, after adding a site, say example.com, it will be accessible using both www.example.com and example.com. You add a domain when creating a site.