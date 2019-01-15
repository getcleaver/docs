## ADDING DATABASE USER
---
### STEPS

1. Select your server and from the secondary sidebar select `Databases`.

2. Switch to `Users` tab.

2. Click `Add New User` button.

3. **NAME**: Name of the database user. The name of the database user must be unique on this server.

4. **PASSWORD**: Password for this database user. This password will be automatically added to your keychain.

5. **CAN ACCESS**: Optionally, select a list of database that you want to allow this user to access. You can always come back and add/remove access later.

4. **DATABASE SERVER TYPE**: You'll only see this field if you haven't installed a database server on your server yet. Select the server you want to install before adding a database user. We recommend [MariaDB][mariadb].

5. Click **Add** button.


## DELETING DATABASE USER
---

### STEPS
1. From the list of database users, click the vertical bar menu (3 vertical dots) next to the database user you want to remove and select `Delete`.

2. Confirm that you really want to delete this database user by clicking **OK** button.

## EDITING DATABASE ACCESS PRIVILEGE
---

### STEPS

1. From the list of database users, click the vertical bar menu (3 vertical dots) next to the database user you want to adjust permissions and select `Edit`. 

2. Add or remove database(s) from the `CAN ACCESS` list.

3. Click **Edit** button to commit the changes.

---

If things are still not clear, or if you are having an issue, please send us an email. In the meantime, watch the following clip that shows how to add a database user to your server using Cleaver.

<br/>


<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/BHUj4UAVikk?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

[mariadb]: https://mariadb.org/