## SECURING YOUR SITE USING FREE LETS ENCRYPT CERTIFICATES
---

Cleaver let's you, with just checking one checkbox, secure your website at the time of creation. While this is convenient, but sometimes you may not want to install the certificates when creating a site esp. if you haven't setup your DNS records yet or for some other reasons. If so, you can always come back and secure your site with free SSL certificates courtesy of [Lets Encrypt][letsencrypt]!

### STEPS

1. Select the site you want to secure with SSL certificates.

2. From the secondary sidebar, select `SSL Certificates`.
3. Click on `ADD Certificates` button.

4. **LET'S ENCRYPT WEBMASTER EMAIL**: The email that these SSL certificates will be registered under. This is where Lets Encrypt will send you emails in case there was a problem with it or in case it needs to be renewed.

5. **DOMAIN TO SECURE**: The domain that needs to be secured. The top level domain should always be included.
You can add additional subdomains if you want by clicking the `+` button. Usually if you are installing certificates for say example.com, you could also include www.example.com and have same certificates applied to both these two domains. In case the domain you are trying to secure is already a subdomain, such as blog.example.com, it usually doesn't make sense to add extra subdomains.
> **⚠️ Warning**: If you haven't set up your DNS records properly and the domains you have entered on this page are not already accessible, the certificate installation process will fail and may invite unwanted side effects. You want to make sure that these domains are accessible first (try to ping them from your terminal to be sure).
    
7. If everything looks ok, click **Add SSL Certificates** button. Cleaver will do a quick DNS lookup for your domains and if it finds a possible problem, it should warn you. You can click **Yes** button to continue.

Wait for few minutes while Cleaver secures your site with free and robust SSL certificates.

> **🗒 Note**: If this is the first secure site on the server then it is going to take few extra minutes to make sure your SSL certificates are as secure as possible.


[letsencrypt]: https://letsencrypt.org/

