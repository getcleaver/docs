## ROLLING BACK A DEPLOYMENT
---
Cleaver's 1-click rollback lets you quickly switch back to a previous deployment. This is really useful in case you realized there was a problem with newly pushed code or in case there was an error during deployment.

### STEPS
1. From the list of deployments, click the vertical bar menu (3 vertical dots) next to the deployment you want to rollback to and select `Rollback`.
2. There is not step 2.

### THINGS TO REMEMBER WITH ROLLING BACK
There are few things you have to keep in mind when rolling back a deployment:

1. Rollback doesn't transfer anything from the linked repository. Rollback only points to a previous snapshot if it already exists on your server.
2. It doesn't make any changes to your linked repository.
3. Rollback is not available for the top/current deployment (you'll notice that the `Rollback` menu is disabled) because it doesn't make sense to rollback to the current deployment.
4. Rollback doesn't revert hooks! This means it doesn't rollback things such as migrations or any database changes that have already been made. Make sure to revert any migrations manually.


