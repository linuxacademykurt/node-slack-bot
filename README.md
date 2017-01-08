# Node Slack Bot

We're going to create a Slack Bot that utilizes [Claudia.js, a Node.js package](https://claudiajs.com/), with AWS Lambda and API Gateway.

1. This first step is optional, but we're going to create a GitHub repository to track our work. You can do the same by creating a repository using your favorite version control system, but again, this isn't required.
2. The second step is going to be installing Node.js on to your local machine. The AWS Lambda service is currently using an older version of Node.js, 4.3.2, so we're going to want to install that version on our local machine or on a Linux Academy server lab if you'd like. You can [download Node.js 4.3.2](https://nodejs.org/download/release/v4.3.2/) from the official source.
  * For Windows, you'll want to download the x64 MSI file for Windows 64-bit builds, or the X86 MSI file for Windows 32-bit builds.
  * For OS-X, you'll want to download PKG file.
  * For Linux, find the appropriate download in the list, or check your Linux distribution's package manager for Node 4.3.2.
  * If you already have a different, newer version of Node.js installed on your machine, download the [Node Version Manager](https://github.com/creationix/nvm/blob/master/README.markdown) from:
3. Now that we have Node installed on our local machine or server lab, we'll want to install the Claudia.JS deployment tool globally by running the following command: npm install claudia -g
4. Now sign up for a [free AWS account](https://aws.amazon.com/). Once logged in to the AWS Console, click on your name and click _Manage Security Credentials_.
  * You should be prompted with an option to "Continue to Security Credentials", or "Get Started with IAM Users". Choose the second option, _Get Started with IAM Users_.
  * Click the Add User button and name it something simple and easy to remember, like "slackbot", and choose to give it _Programmatic accesss_. Click _Next: Permissions_.
  * On this screen, choose to _Attach existing policies directly_, we're going to want to attach the following three policies by searching for them one at a time and clicking the checkbox next to them:
    * AWSLambdaFullAccess, IAMFullAccess and AmazonAPIGatewayAdministrator.
  * Click _Next: Review_, and if you see the three policies, choose to _Create User_.
  * Now that you have created the user, you're going to want to store them on your local machine. If you don't already have a local AWS credentials file, create one - On Mac or Linux, it'll be at ~/.aws/credentials, on Windows it'll be C:\Users\YOUR_USER_NAME\.awscredentials
  * Enter the following in the credentials file, replacing the placeholder values with the values you can view after creating the IAM user.
  ```
  [slackbot]
  aws_access_key_id = YOUR_USERS_ACCESS_KEY_ID
  aws_secret_access_key = YOUR_USERS_SECRET_ACCESS_KEY
  ```
5. Create a new directory to house your project if you haven't already: `mkdir node-slack-bot` and then `cd node-slack-bot`. Now run `npm init --yes`, the yes flag just tells the init command to accept all the default values.
6. Now let's install Claudia.js globally by running `npm install claudia -g`. Verify that it installed correctly and is at least version 1.4.0 or greater by running `claudia -v`. Now, let's install the Claudia.js bot builder directly to our project. Make sure you're in your project directory (node-slack-bot), and run `npm install claudia-bot-builder --save`
