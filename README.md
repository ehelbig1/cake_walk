# Alexa Skill Development

[ASK-CLI Documentation](https://developer.amazon.com/en-US/docs/alexa/smapi/quick-start-alexa-skills-kit-command-line-interface.html)

## ASK-CLI

To install ASK-CLI run
`npm install -g ask-cli`

You will need to have an AWS account and an IAM user with the correct permissions (call these out later).

You will need:
- Access Key
- Secret Access Key

From this account in order to configure the ASK-CLI.

If you've already set up the AWS-CLI then you can find these credentials in ~/.aws/credentials.

These credentials can also be found in the AWS Console.
- Navigate to the IAM service
- Select Users from the left menu
- Create a new Access Key (The Secret Access Key is only accessible immediately after creating a new Access Key)
	- This will present you with the new Access Key and Secret Access Key

### Initialization

To set up/initialize ASK-CLI, run
`ask init`

The first time you run this you will be redirected to your browser to allow access to your account.
You will then be asked for the Access Key and Secret Access Key of a user on you AWS account (mentioned above)

## Source Control

Each developer should have their own AWS account and Alexa Console.

When first joining the project, the developer should setup the ASK-CLI and then create a new project by runninng
`ask new`  

Delete current git repository
`rm -rf .git`

Initialize a new git repository
`git init`

Add a remote repository
`git remote add origin {project repository}`

Save new skill.json
`git add skill.json`
`git ci -m "Saving skill.json`

Fetch the current code from the repository.
`git fetch`

Reset repository history
`git reset --hard origin/master`

Get stored skill.json
`git reflog` - make note of the commit hash
`git co origin/master -- skill.json`

Add skill.json to .gitignore

Work with normal git flow.

When you have changes ready to test run
`ask deploy`

