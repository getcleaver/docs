
## DEPLOYING FROM A REMOTE REPOSITORY

Cleaver lets you deploy from a remote repository on either GitHub, GitLab, or BitBucket. Cleaver supports both private and public repositories.

Switch repository from a one version control provider (GitHub, GitLab, or BitBucket) to to another is seamless and you don't lose anything, including your old deployments. This means you could still rollback to an old deployment if you need to.

### PREREQUISITES

If you have provisioned your server before Cleaver v0.20, you **MUST** update your server. Cleaver will let you know if your server needs to be updated. It only takes a few seconds to apply the update needed for supporting remote repository deployment.

### STEPS
1. Go to your VCP, and create and copy a new personal access token. This differs for each VCP. See steps below for each provider.
2. Back in Cleaver, select `Providers` from the sidebar and click `Add New Provider`.
3. Select your VCP - either GitHub, GitLab, or BitBucket and enter a profile name for this provider. Paste the personal access token that you created in step 1 above in the Access Token field. Click `Add` when you are done.
4. Select the site you are trying to deploy and select `Repository` tab.
5. In the `REMOTE REPOSITORY` field, copy paste your git project like so: `getcleaver/docs`.
6. Add default branch to deploy from in `DEFAULT BRANCH TO DEPLOY` field. Don't worry, you can always deploy from a different branch if you need to.
7. Hit `Done` button and now you are ready to deploy from your remote repository!

#### GETTING PERSONAL ACCESS TOKEN FROM GITHUB
`. Go to https://github.com/settings/tokens/new and create a new personal access token.
2. Select **repo** scope.

#### GETTING PERSONAL ACCESS TOKEN FROM GITLAB
1. Go to https://gitlab.com/profile/personal_access_tokens and create a new personal access token.
2. Leave the `Expires At` field blank and select **api** scope.

#### GETTING PERSONAL ACCESS TOKEN (APP PASSWORD) FROM BITBUCKET
1. Go to https://bitbucket.org/account
2. From the sidebar and from under ACCESS MANAGEMENT, select `App passwords`.
3. Click `Create app password` button.
4. Give it a label and select `Repositories>Read` permission.
