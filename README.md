# LWC Boilerplate - Not Working...

I am trying to get a hello-world going with LWC (open source!!!), to run it as a stand-a-lone webpage/website, so that I can embed it in an existing website (running on Apache + PHP)

I followed this guide: [https://lwc.dev/guide/install](https://lwc.dev/guide/install)

```
npm init lwr        # Follow the on-screen instructions
                    # Select the "Single Page App" project
                    # Select the "LWC" variant
cd YourProjectName
npm install
npm run start      
```
The npm run start, works fine and the "Hello World" page is work at http://localhost:3000

Then I went to the #WebPack section installed the webpack and packages,
```
npm install --save-dev webpack webpack-cli lwc-webpack-plugin lwc @lwc/module-resolver
```
created the config files, added the demo app, but got the following error when I ran `npx webpack build`:

```
user@work lwr-final]$ npx webpack build
[webpack-cli] Failed to load '/home/user/Projects/lwc/lwr-final/webpack.config.js' config
[webpack-cli] ReferenceError: module is not defined in ES module scope
This file is being treated as an ES module because it has a '.js' file extension and '/home/user/Projects/lwc/lwr-final/package.json' contains "type": "module". To treat it as a CommonJS script, rename it to use the '.cjs' file extension.
    at file:///home/user/Projects/lwc/lwr-final/webpack.config.js:3:1
    at ModuleJob.run (node:internal/modules/esm/module_job:194:25)
```
I went through the install guide a number of times with each time a fresh/clean install, but every time the same error. (Running on Fedora linux v38)

Does anyone know what the issue might be?
Am I doing something wrong or is the setup-guide missing a few steps?