## PROVISIONING SERVER ON DIGITALOCEAN

---

> **🗒 Note**: Make sure you have authorized Cleaver to create and administer servers on DigitalOcean by adding an access token. If not, perform [these steps][1] first.

#### STEPS

1. Select **Servers** menu from the sidebar.

2. Click **Add New Server** button from the top-right corner.

3. If it has not already, let Cleaver fetch the latest available specs from DigitalOcean. This should take no more than few seconds.

4. **SERVER NAME**: Cleaver should have created a server name for you. You can change it if you want. Server name must be unique for the selected cloud provider.

5. **PROVIDER PROFILE**: Select the profile you want to use for creating this server. If you have multiple profiles, make sure you have selected the correct one.

6. **SERVER SIZE**: Select the size of the server you want to create. You can see the full specs of each size by checking the `show specs` checkbox. Make very sure that you have selected the right size.

7. **SERVER REGION**: The location of the data center where your server will be created.

8. **DATABASE SERVER TYPE**: Select the database server you want to install when provisioning. This is optional and you can only choose one. If you want, you can skip this for now as you can always install this later.

9. **LANGUAGES**: Select languages to be installed during provisioning. You can pick multiple languages. You don't have to decide what to install right now. When you create a site later, the appropriate languages and libraries will be installed for you. However, it's a good idea to install them now if you already know you are going to need them.

10. Verify all the choices you have made one more time and click the **Add** button.

Sit back and relax! Based on what have selected to install and the location you have selected, Cleaver is going to take anywhere from 5 to 10 minutes to get the server ready for you. You can keep your eye on the `status` column to see what Cleaver is doing on the server.

> **🗒 Note**: The sudo password for this server will be automatically generated and set for you and should be displayed at the top. This password is automatically saved in your keychain as well. You should note down this password and put it in a safe place just in case.

<br/>

> **⚠️ Warning**: Don't rename, edit, or delete any password created by Cleaver from the keychain.

If things are still not clear, please watch [this][2] clip that shows how to provision a DigialOcean server.

<br/>

[1]: ../2%20Cloud%20Providers/Adding%20DigitalOcean%20Profile.md
[2]: https://www.youtube-nocookie.com/embed/Ly9POjhqpDY?rel=0
[ssl-certificates-later]: ../SSL%20Certificates.md
