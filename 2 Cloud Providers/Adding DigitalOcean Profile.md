## ADDING DIGITALOCEAN PROFILE
---

To allow Cleaver to use your DigitalOcean account so that it can create and administer new servers, you first need to add an access token from your DigitalOcean account to Cleaver. This is one time thing and don't have to do it again unless you revoked or edited the access token.

#### STEPS

1. Go to https://cloud.digitalocean.com/settings/api/tokens and click **Generate New Token** button.

2. On the modal box that appears, provide a name for this token; something that you could remember later, such as **Awesome Cleaver**.

3. Make sure that both `Read` and `Write` scopes are selected. Cleaver will not be able to provision a server for you without the `Write` permission.
4. Click **Generate Token** button.

5. Copy the access token, switch to Cleaver app, and select **Providers** menu from the sidebar.

6. Click the **Add New Provider** button.

7. Once on the Add New Provider page make sure to select `DigitalOcean` tab.

8. **PROFILE NAME**: The name of this profile. If you have multiple providers and/or profiles, this name is going to be important when creating a new server.

9. **ACCESS TOKEN**: The token that you copied from DigitalOcean in step 5.

10. Once you are done, click the **Add** button.

Cleaver will verify your token with DigitalOcean and if everything goes well, you should see your new token name listed on the `Providers` page. And in case you were wondering, the access token is saved in your keyring.

If things are still not clear, or if you are having an issue, please send us an email. In the meantime, watch the following clip that shows how to add a DigitalOcean access token.

<br/>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/9EKtO_KfQvc?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>