# Azure Active Directory OIDC Web Sample - Node.js

This Node.js app will give you with a quick and easy way to set up a Web
application in node.js with Express usind OpenID Connect. The sample server
included in the download are designed to run on any platform.

We've released all of the source code for this example in GitHub under an MIT
license, so feel free to clone (or even better, fork!) and provide feedback on
the forums.

## Quick Start

### Requirements:

[Node.js](https://nodejs.org/en/)

### Step 1: Download the Sample application and modules

Clone the sample repo and install the NPM.

From your shell or command line:

* `$ git clone https://github.com/xby2/Azure-AD-SAML-POC-NodeJS.git`
* `$ npm install`

### Step 2: Configure your server

Provide the parameters in `exports.creds` in config.js as foillows:

1. identityMetadata - should use the following URL:
   "https://login.microsoftonline.com/xby2llc.onmicrosoft.com/.well-known/openid-configuration"
1. clientID - the Application ID provided by the app in Azure AD.
1. clientSecret - the key to access the application inside Azure AD.

If needed, the above can be provided by the Azure AD Administrator (Dave F.)

* Set `exports.useMongoDBSessionStore` in config.js to false, if you want to use
  the default session store for `express-session`. Note that the default session
  store is not suitable for production, you must use mongoDB or other
  [compatible session stores](https://github.com/expressjs/session#compatible-session-stores).

### Step 3: Run the application

* Run the app. Use the following command in terminal.

```
$ node app.js
```

**Is the server output hard to understand?:** We use `bunyan` for logging in
this sample. The console won't make much sense to you unless you also install
bunyan and run the server like above but pipe it through the bunyan binary:

```
$ npm install -g bunyan
$ node app.js | bunyan
```

### You're done!

You will have a server successfully running on `http://localhost:3000`.

### Acknowledgements

We would like to acknowledge the folks who own/contribute to the following
projects for their support of Azure Active Directory and their libraries that
were used to build this sample. In places where we forked these libraries to add
additional functionality, we ensured that the chain of forking remains intact so
you can navigate back to the original package. Working with such great partners
in the open source community clearly illustrates what open collaboration can
accomplish. Thank you!

## About The Code

Code hosted on GitHub under MIT license
