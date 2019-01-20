
## DEPLOYING FROM A REMOTE REPOSITORY

Cleaver lets you deploy either from a local repository on your computer or from a remote repository on either GitHub, GitLab, or BitBucket. Deploying from a local repository is about 3 times slower than deploying from a remote repository and this only gets worse once your project becomes larger. Even if only for this reason, we highly recommend that you deploy from a remote repository. Cleaver supports both private and public repositories.

Switch repository from a local path to a remote URL and vice-versa is seamless and you don't lose anything, including your old deployments. This means you could still rollback to an old deployment if you need to.

### PREREQUISITES
1. git must be installed on your local machine.
2. If you have provisioned your server before Cleaver v0.20, you must update your server. Cleaver will let you know if your server needs to be updated. It only takes a few seconds to apply the update needed for remote repository deployment.
2. You must use full SSH URL of your project e.g. `git@github.com:getcleaver/docs.git`
3. You must add public keys of both your local machine and your actual server provisioned by Cleaver to your VCS provider (GitHub, GitLab, or BitBucket). You can get the public key of your server from within Cleaver itself.

### STEPS
1. In Cleaver, select your server where your app will be deployed, go to SSH Keys, and copy Server public SSH Key. The key starts with **ssh-rsa**.
2. Now go to your VCS provider, select your repository, add the copied public SSH key from step 1 as a deploy key. This differs for each VCS provider. See steps below for each provider.
3. Go back to your local machine, copy your public key ssh key (generally found in `~/.ssh/id_rsa.pub`), and add this key as a deploy key as well. If you could already push to your repository from your local machine, then you can skip this step as that means you already have access to this repository.
4. In Cleaver, select the site you are trying to deploy, select `Repository` tab and select `Remote Repository`.
5. In the `REMOTE PROJECT GIT REPO` field, copy paste full SSH URL of your project like `git@github.com:getcleaver/docs.git`. You **must** add SSH URL and **not** https URL.
6. Hit `Done` button and now you are ready to deploy from your remote repository!

#### ADDING DEPLOY KEY TO GITHUB
1. Select your repository, click `Settings` tab at the top (next to *Insights* tab), and select `Deploy Keys` from the sidebar.
2. Click on `Add deploy key` and add your key.

#### ADDING DEPLOY KEY TO GITLAB
1. Select your repository, click `Settings > Repository` from the sidebar
2. Expand `Deploy Keys` and add your key.

#### ADDING DEPLOY KEY TO BITBUCKET
1. Select your repository, click `Settings` from the sidebar, from the nested sidebar, select `Access keys` item
2. Click `Add key` and add your key.