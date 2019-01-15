## ADDING LARAVEL APP
---

### STEPS

1. Select the server you want to add this Laravel site to.

2. Select `Sites` menu from the secondary sidebar. 

3. Click the **Add New Site** button.

4. **DOMAIN NAME**: Domain name for this site like laravel.example.com. You must provide this value.

5. **ALSO ADD DNS RECORDS**: If you check this checkbox, Cleaver will add an [A record][dns] for your domain as well as a [www CNAME][dns]* for your domain. This basically means that if you added a site, say example.com, Cleaver configures your domain records with your cloud provider so that eventually you will be able to access your website using both example.com and www.example.com. This will only work if you have pointed your domain to the nameservers of the selected cloud providers (such as ns1.digitalocean.com, ns1.vultr.com etc)

5. **PROJECT TYPE**: Select **Laravel**.

6. **SECURE WITH LET'S ENCRYPT**: Check this field if you want to install and configure SSL certificates (from Let's Encrypt) for this site. We highly recommend you to check this option; after all it's free! If you decide to check this field and install SSL certificates, you must provide a valid email address.
> **⚠️ Warning**: If you have not checked the checkbox in step 5 to let Cleaver configure DNS records for you, make sure you domain is pointed to the nameservers of the selected cloud provider otherwise this setup will fail.
> **🗒 Note**: In case you decided not to secure your site with free SSL certificates at this time, you can always [install SSL certificates and secure your site later](/ssl-certificates.md).

7. Double check that all the values are what you wanted and then click **Add** button.

Cleaver will finish installing and configuring the site for you within a couple of minutes. Among few other Laravel dependencies, Cleaver also installs PHP and NodeJS if you didn't install them when provisioning the server. Redis Server and Memcached will be installed as well. All these could add extra minutes to finish creating the site.

> **🗒 Note**: If this is the first secure site on the server then it is going to take few extra minutes to make sure your SSL certificates are as secure as possible.

Once it is done, you can visit this site on your browser. You should see a the output of `phpinfo()` on the page.

> 🍄 Just for fun, after Cleaver is done adding your site, you could go to https://ssllabs.com/ssltest/analyze.html to check what security grade your site gets. It should get at least an A because you deserve nothing less!


If things are still not clear, or if you are having an issue, please send us an email. In the meantime, watch the following clip that shows how to create a secure Laravel site using Cleaver.

<br/>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/ZpfERBqgBfQ?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

