## ADDING VULTR PROFILE
---

To allow Cleaver to use your Vultr account so that it can create and administer new servers, you first need to add a personal access token from your Vultr account to Cleaver. This is one time thing and don't have to do it again unless you revoked or edited the access token.

#### STEPS

1. Go to https://my.vultr.com/settings/#settingsapi and make sure to select **API** tab.

2. If API access isn't enabled, click **Enable API** button to enable it.

3. In the **Access Control** panel, click on **Allow All IPv4** button to allow to use API from your desktop.

4. On the modal box that appears asking you to confirm, click on **Ok**.

4. Copy the API key, switch to Cleaver app, and select **Providers** menu from the sidebar.

5. Click the **Add New Provider** button.

6. Once on the Add New Provider page make sure to select `Vultr` tab.

7. **PROFILE NAME**: The name of this profile. If you have multiple providers and/or profiles, this name is going to be important when creating a new server.

8. **ACCESS TOKEN**: The token that you copied from Vultr in step 5.

9. Once you are done, click the **Add** button.

Cleaver will verify your token with Vultr and if everything goes well, you should see your new token name listed on the `Providers` page.

If things are still not clear, or if you are having an issue, please send us an email. In the meantime, watch the following clip that shows how to add a Vultr personal access token to Cleaver. And in case you were wondering, the access token is saved in your keyring.

<br/>

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/x80xhiAS7Ro?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>