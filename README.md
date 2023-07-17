# Get an activation key
We use an activation key to register the containers on GitHub.  If these instructions fail, see [Creating Red Hat Customer Portal Activation Keys](https://access.redhat.com/articles/1378093)

1. You must have a RHEL subscription to do this.  If you need one and you may be able to use the Developer Subscription for Individuals.  See "Get a D4I Subscription" below.
2. 1. Visit the [Activation Key Management Page](https://console.redhat.com/settings/connector/activation-keys)
3. Click "Create activation key"
4. Choose an appropriate name, role, SLA, and usage
5. Set Auto Attach to "Enabled"
6. Select the "Red Hat Developer Subscription for Individuals" subscription to be auto attached
7. Click "Create"
8. Click "Cancel" if prompted to create a new key.
9. Record your Org ID

# Save the secrets in GitHub for use with your jobs
For details see [Creating encrypted secrets for a repository](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository)

1. Go the main page of the repository and click "Settings"
2. Go to "Security->Secrets and Variable->Actions"
3. Using the "New repository secret" button add your Organization ID as a secret called ORG_ID and your Activation Key Name as a secret called "ACTIVATION_KEY"

# Testing in a fork
1. With a new user, create a fork of the repository.  Enable Actions.
2. Make any update and push a commit.  This should fail at the registration step.
3. Go the main page of the repository and click "Settings"
4. Go to "Security->Secrets and Variable->Actions"
5. Using the "New repository secret" button add your Organization ID as a secret called ORG_ID and your Activation Key Name as a secret called "ACTIVATION_KEY"
6. Make another update, this should work.

## PR from a fork
1. In your fork from "Testing in a fork" send a PR to the main repository
2. In that repository, as the repository owner, you may need to click "Approve and run" in the PR.
3. It should work.

# Get a D4I Subscription
1. Go to the [Developer Portal](https://developers.redhat.com/products/rhel/overview) and click "Download RHEL at no-cost"
2. When prompted, create a new Red Hat account and accept the terms and conditions
3. You can cancel the download as you don’t need the iso.
