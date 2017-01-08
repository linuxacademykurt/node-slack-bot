# Node Slack Bot

This first step is optional, but we're going to create a GitHub repository to track our work. You can do the same by creating a repository using your favorite version control system, but again, this isn't required.

The second step is going to be installing Node.js on to your local machine. The AWS Lambda service is currently using an older version of Node.js, 4.3.2, so we're going to want to install that version on our local machine or on a Linux Academy server lab if you'd like. You can [download Node.js 4.3.2](https://nodejs.org/download/release/v4.3.2/) from the official source.

For Windows, you'll want to download the x64 MSI file for Windows 64-bit builds, or the X86 MSI file for Windows 32-bit builds. For OS-X, you'll want to download PKG file. For Linux, find the appropriate download in the list, or check your Linux distribution's package manager for Node 4.3.2.

If you already have a different, newer version of Node.js installed on your machine, download the [Node Version Manager](https://github.com/creationix/nvm/blob/master/README.markdown) from:

Now that we have Node installed on our local machine or server lab, we'll want to install the Claudia.JS deployment tool globally by running the following command:
npm install claudia -g

Now sign up for a [free AWS account](https://aws.amazon.com/).