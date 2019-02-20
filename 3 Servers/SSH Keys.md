## SSH KEYS
---

When you create a server, Cleaver automatically adds a public SSH key to your server. The private counterpart of this public SSH key can be found under `~/.ssh/cleaver` folder on macOS/Linux. Cleaver also adds a private key on the provisioned server itself and if you go to `Servers > <your server name> > SSH Keys`, you can see its public counterpart. You use this key when you need to let other third party services access your server.

For security reason, Cleaver disables disables password login. User `cleaver` is created and used by Cleaver to run tasks on your server.

### SSHing into your server using the default SSH key
---
On MacOS or Linux, from the terminal you can run the following command:

`ssh cleaver@<server-ip-address> -i ~/.ssh/cleaver/<server-private-key>`

### Adding additional SSH Keys
---
In addition to the default key that Cleaver added for you, you can add additional SSH keys to your server - as many as you want.

#### STEPS

1. Select a server then select `SSH Keys`from the sidebar.

2. Click `Add New Key`button.

3. **NAME**: The name of the key. This name must be unique for the selected server.

4. **PUBLIC KEY**: The public key that you want to copy to your server. <br/>**Pro tip**: On macOS, you can run something like `cat ~/.ssh/id_rsa.pub | pbcopy` on your terminal to copy the contents of `~/.ssh/id_rsa.pub` to your clipboard.

5. Click **Add** button.

If you want to verify whether the key was really added to your server, you could try to login using the private pair of the key that you just added:

`ssh cleaver@<server-ip-address> -i ~/.ssh/id_rsa`

Or, you could log into your server and verify that the key was appended to `/home/cleaver/.ssh/authorized_keys`.

**⚠️ Warning**: Don't modify `/home/cleaver/.ssh/authorized_keys` by hand otherwise you may not be able to login to your server and/or Cleaver may not be able to run administer your server. Use Cleaver to manage your keys.


### Deleting SSH Keys
---

### STEPS

1. Select the server you want to delete a SSH key from.

2. From the list of SSH key, click the vertical bar menu (3 vertical dots) next to the key you want to remove and select `Delete`. <br/>
The key will be deleted immediately **without** asking for confirmation.


If things are still not clear, or if you are having an issue, please watch [this][ssh-clip] clip that shows how to manage SSH keys using Cleaver.

<br/>

[1]: https://unix.stackexchange.com/a/82639/249514
[ssh-clip]: https://www.youtube-nocookie.com/embed/s4xTsITVQ3M?rel=0
