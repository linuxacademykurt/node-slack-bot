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
