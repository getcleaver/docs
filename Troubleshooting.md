## GETTING STARTED TROUBLESHOOTING
---

* **I cannot sign in**
    * Make sure you have created a Cleaver account. You can create an account from within the app. It only takes few seconds to signup for a new account. 


## CLOUD PROVIDER TROUBLESHOOTING
---

* **I cannot sign in**
    * Make sure you have created a Cleaver account. You can create an account from within the app and only takes few seconds.
    
    
* **I keep getting 'Error adding the profile' error**
    * Make sure the access token you copied exists on the provider and is valid.
    

## SERVER PROVISION TROUBLESHOOTING
---

* **I don't see a list of server region**
    * Hit `cancel` button and try again by clicking `Add New Server` button. If you still can't see the list, try restarting the app.
    
    
* **Server status is 'error' and I don't know why**
    * First, make sure your access token is valid.
    * This is a known issue with DigitalOcean sometimes. Go to your [DigitalOcean Dashboard][do-dashboard] and see if it says "There was an error while creating your droplet" next to your droplet. In either case, try creating a new server again. If the problem persists, wait for few minutes and try creating a server on a different region.
    * Check [DigitalOcean status page][do-status] and make sure the region you have selected is not having an issue.
    * If everything seems fine and nothing works, please send us an email.
    
    
* **Server provisioning is taking forever**

    * Server provisioning duration could depend on few factors:
        * The region you have selected.
        * DigitalOcean is going through a maintenance or experiencing some issues.
        * Extra packages you have selected (such as MySQL, NodeJS) etc. and the status of these packages.
        * Your network is slow (not a big factor but still) or got interrupted while provisioning.
    Sometimes it is helpful to just let it run for extended time. Also, you want to go to DigitalOcean dashboard and see if there was an error or not.
    Try restarting the app and provisioning a new server possibly on a different region.
    
    
* **I cannot login to my server as root**
    * Once your server is initially provisioned, logging as root user over SSH is disabled by Cleaver because of [security concerns][1]. Try to login as user `cleaver` which is created for you by Cleaver when provisioning your server. 

* **Where is the private key for a server that I just created?**
    * On macOS, it's under `~/.ssh/cleaver` and starts with the nave of the server followed by a random id.
        
    
* **I cannot login as user `cleaver` over ssh**
    * Make sure to you pass in your private key located under `~/.ssh/cleaver` when logging in. Something like:
    
    `ssh cleaver@<server-ip-address> -i ~/.ssh/cleaver/<server-private-key>`
    

## SITE TROUBLESHOOTING
---

* **Installing Let's Encrypt fails or my site is not encrypted**
    * There could be a number of reasons why Let's Encrypt SSL certificates would fail:
        * Make sure you own the domain you are adding
        * Make sure the domain is pointed to the cloud server's nameservers (for DigitalOcean it would be ns1.digitalocean.com, ns2.digitalocean.com, and ns3.digitalocean.com) that you are adding this site to.
        * Make sure there isn't already a site running with this name somewhere else.
        * Make sure you are not creating too many secure sites on this server. Let's Encrypt allows you to create only [5 certificates per hour][letsencrypt-rate-limit] on 1 server.
    
* **Let's Encrypt configuration is taking forever**
    * If you are adding a secure site for the first time, SSL certificate configuration could take some extra minutes as we create a [dhparam][dhparam] file for extra security. Unfortunately, there is no way to know how long it would take - it could take anywhere from 3-4 minutes to 30 minutes or more. But we have never seen it go beyond 10 minutes ourselves.
    
    Creation of the dhparam file only happens on the first SSL site creation, so you should not see SSL certicates configuration taking too much time every time you add a new site. If it does, let us know and we'll figure it out together.
    
* **I have other questions or I'm still having an issue**
    * We are very sorry that you are still having an issue. Please email us with as much information as possible and we'll sort it out right away.

## DATABASE TROUBLESHOOTING
---

* **My MySQL setup has an issue**
    * MySQL sometimes does not play well with installation scripts. This is also one of the reasons why we strongly recommend [MariaDB][mariadb]. But if you cannot switch to MariaDB, try installing MySQL again by logging into your server. You can [follow these steps][2].
    

## DEPLOYMENT TROUBLESHOOTING
---

* **Deploy Now button is disabled**
* Make sure you have added a path to your local git repo. If you have not, click on `⚙️ Settings` button to [link your repo][setup-repo] first.
    
    
* **My .env variables are not synced when deploying**
    * This is by design. Go to `Environment` tab to sync it manually.
    
    
* **My changes are not being deployed**
    * Make sure that you have committed all your changes before you want to deploy. This is by design as well.
    * Make sure you have set the branch that you intend to deploy on the [setup repo page][setup-repo]    
    
    
* **Deployment fails sometimes but then deploying it again works**
    * Make sure to wait at least a minute before deploying a new deployment.
    If you click `🚀 Deploy Now` button too many times consecutively, you may have been throttled by your own server.
    

* **The Rollback button on the first/ top deployment is disabled**
    * This is by design as it really doesn't make sense to rollback to the current deployment. If you have a good case against it, please let us know.

    
[setup-repo]: /deployments/setup-local-repo

[mariadb]: https://mariadb.org/
[2]: https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04
    
[mariadb]: https://mariadb.org/
[2]: https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-16-04
[letsencrypt-rate-limit]: https://letsencrypt.org/docs/rate-limits/
[dhparam]: https://security.stackexchange.com/questions/94390/whats-the-purpose-of-dh-parameters

[1]: https://unix.stackexchange.com/a/82639/249514
[do-dashboard]: https://cloud.digitalocean.com/droplets
[do-status]: http://status.digitalocean.com/