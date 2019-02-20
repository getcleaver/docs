## ADDING GRAV CMS
---

### STEPS

1. Select the server you want to add this [Grav][1] site to.

2. Select `Sites` menu from the secondary sidebar.

3. Click the **Add New Site** button.

4. **DOMAIN NAME**: Domain name for this site like grav.example.com.

5. **ALSO ADD DNS RECORDS**: If you check this checkbox, Cleaver will add an [A record][dns] for your domain as well as a [www CNAME][dns]* for your domain. This basically means that if you added a site, say example.com, Cleaver configures your domain records with your cloud provider so that eventually you will be able to access your website using both example.com and www.example.com. This will only work if you have pointed your domain to the nameservers of the selected cloud providers (such as ns1.digitalocean.com, ns1.vultr.com etc)

5. **PROJECT TYPE**: Select **Grav**.

6. **ADD ADMIN PLUGIN**: Check this field to install Grav with [admin plugin][2].

7. **SECURE WITH LET'S ENCRYPT**: Check this field if you want to install and configure SSL certificates (from Let's Encrypt) for your Grav site. We highly recommend you to check this option; after all it's free! If you decide to check this field and install SSL certificates, you must provide a valid email address.
> **⚠️ Warning**: If you have not checked the checkbox in step 5 to let Cleaver configure DNS records for you, make sure you domain is pointed to the nameservers of the selected cloud provider otherwise this setup will fail.
> **🗒 Note**: In case you decided not to secure your site with free SSL certificates at this time, you can always [install SSL certificates and secure your site later][ssl-certificates-later].

8. Double check that all the values are what you wanted and then click **Add** button.

Cleaver will finish installing and configuring the site for you within a couple of minutes. Among few other Grav dependencies, Cleaver also installs PHP if you didn't install it when provisioning the server.

> **🗒 Note**: If this is the first secure site on the server then it is going to take few extra minutes to make sure your SSL certificates are as secure as possible.

Once it is done, you can click on a little arrow to visit the site on your browser. Make sure that it's served over https and not http.

> 🍄 Just for fun, after Cleaver is done adding your site, you could go to https://ssllabs.com/ssltest/analyze.html to check what security grade your site gets. It should get at least an A because you deserve nothing less!

<br/>


If things are still not clear, or if you are having an issue, please watch [this][site-clip] clip that shows how to create a secure Grav cms site with the admin plugin using Cleaver.

<br/>
\* www CNAME is only added for a domain and not for a sub-domain

[1]: https://getgrav.org
[2]: https://github.com/getgrav/grav-plugin-admin/blob/develop/README.md
[site-clip]: https://www.youtube-nocookie.com/embed/1Xfl8ARLq28?rel=0
[ssl-certificates-later]: ../SSL%20Certificates.md
[dns]: https://www.name.com/support/articles/205516858-Understanding-DNS-record-types
