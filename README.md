# NPM cheat sheet

Following is a list of commands used  
npm init  - initialize npm and create package.json  
npm install express - install express  
npm install babel-cli babel-stage-0 babael-preset-es2015 --save-dev  - installing babel dependencies as dev and hence will not be used in production build  
npm install -g react  - global install of react  
npm install create-react-app -g  - global install of create-react-app  
npm install esling@5.2.0 -g - globally installing a specific version of eslint using the @.  
npm outdated  - command to check outdated dependencies.  
npm outdated -g  - command to check outdated dependencies globally.  
npm update eslint - updates package, may not work always and should just use npm install instead.  
npm uninstall babel-preset-es2015 - remove es2015 package  
npm install babel-preset-env --save-dev  - installing the correct env preset according to .babelrc file as dev  
versioning syntax 1.4.2: 1-> major release like a new vversion of s/w, 4-> minor release or feature update, 2-> patches and bug fix  
^1.x.x: The ^ is the default for installing new packages meaning latest version of package version 1 will be installed npm won't install any version beyond that  
`~1.5.x: A more strict approach meaning latest version of package 1.5 will be installed npm won't install any version beyond that  
For specific version remmove the ^/`~ in the verison number  
When you do npm install, package.json is the input and package-lock.json is the output. Always commit package-lock.json as it will limit the version installed in the package.json file to the version specified in the package-lock.json.  
npm cache verify  - gives a report on the cache  
npm cache clean --force - forcefully cleans cache. As cache self cleans after version 5 it has to be done forcefully or it won't work.  
npm audit - checks the dependencies in the project and makes sure that they are safe to use. Works with npm version 6 and above.  
docs.npmjs.com/misc/scripts - has all the predefined properties that can be used in npm scripts.
nodemon - Nodemon is a utility that will monitor for any changes in your source and automatically restart your server. Perfect for development. Install it using npm.  
"scripts": {  
    "start": "nodemon ./index.js --exec babel-node -e js"  
  } nodemon runs the index.js file but we make sure to use babel first to convert the exec code into readable code for the web.  
How to run your own presets that are not in the predefined list: npm run name-of-your-preset  
npx -p @angular/cli ng new myapp    -   this command temporarily installs the angular cli tool with -p(package) and then use the comand from that package to create a new app without having to the package preinstalled in your system  
npx mocha   -   mocha is a javascript test framework and using npx you can temporarily install it and use it.  
An interesting command to run is npx cowsay message goes here  
Alternatives to npm -   yarn: similar to npm but is faster and does requier to install a packager
                        ni: same as yarn and npm but uses a less verbose approach
