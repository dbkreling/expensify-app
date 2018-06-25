Executive summary:

  To run this project, navigate to the root of the project (expensify-app/) and from a terminal issue:

    $ yarn run serve

  and from another terminal window:

    $ yarn run dev-server

Needless to say that the dev-server output will show where the project is running at by showing a line like:

    "Project is running at http://localhost:8081/"

Your browser should resolve that with no issues.

See below for further information about the project.

Description:

This is a project from The Complete React Web Developer Course (with Redux) course.

To install all the dependencies of this project, run:

  $ yarn install

The dependencies for this project (as of now) are

1) Nodejs (from the web)

2) Yarn (installed via npm

3) Preferably Visual Basic Studio (from the web)

4) live-server (installed via yarn. Make sure to add ~/.yarn to the PATH)

5) Babel - v.6.24.1 (via yarn global add babel-cli@6.24.1)
  5.0) yarn init
  5.1) locally install env preset via yarn
  5.2) locally install react preset via yarn

	$ yarn add babel-preset-react@6.24.1 babel-preset-env@1.5.2


6) Create a new src/app.js file with the contents of public/scripts/app.js.
   Now the scripts/app.js will not be touched anymore.

  From a terminal session issue:

    - babel src/app.js --out-file public/scripts/app.js --presets=env,react --watch

  ... to watch what files have been automatically changed after the changes we made

  From another session, issue

    - live-server public

  ... to start serving up the public directory

   Do your changes in the src/app.js file from now on.


7) Visual Studio extension: Babel ES6/ES7


8) Browser addOn / Plugin: 'React Developer Tools'
    Installation directly via browser


9) On Lecture 49-Avoid Global Modules, we uninstall live-server and babel-cli[i] from the
global modules and reinstall them as local dependencies. The sequence of commands, for the
records, are:

   $ yarn global uninstall live-server babel-cli

   And then:

   $ yarn add live-server babel-cli@6.24.1


10) From lecture 53 and 54, install validator, react, react-dom, babel-core and babel-loader.
Babel-core and babel-loader are necessary in order to connect Babel with webpack.

   $ yarn add validator@8.0.0 react@16.0.0 react-dom@16.0.0 babel-core@6.25.0 babel-loader@7.1.1


11) From lecture 57, install webpack dev-server replacing live-server, because it comes with some optimizations to process and reder webpack code to the screen.

    $ yarn add webpack-dev-server@2.5.1

  And then configure it as contentBase in order to point the public folder to the server.

    Documentation can be found at https://webpack.js.org/configuration/dev-server


12) Instal transform-class-properties plugin, found at http://babeljs.io/docs/plugins/transform-class-properties/, by issuing:

    $ babel-plugin-transform-class-properties

    ... and restart the dev-server.

    To restar the dev-server, issue 
      $ yarn run dev-server



13) Set up React Modal, which is accomplished by issuing:

    $ yarn add react-modal@2.2.2

    .. and restart the dev-server.

    Docs found at https://github.com/reactjs/react-modal

14) CSS-Loader

  Documentation: npmjs.com/package/css-loader

  Installation:

    $ yarn add css-loader@0.28.4 style-loader@0.18.2

15) Style-loader

  Documentation: npmjs.com/package/style-loader

  Installation:

    $ yarn add style-loader@0.18.2

To add 14 and 15, the steps are:

  a. create a ./styles/styles.css at the root directory;
  b. in webpack.config.js, add a new rule under 'module' (see lecture 64 for further instructions);
  c. add steps 14 and 15
  d. import './styles/style.css' into app.js

  IMPORTANT: Restart your dev-server

  Go ahead and configure scss now:

  https://sass-lang.com/guide


16) Add two new loaders:

  sass-loader: allows you to import sass files

  node-sass: converts scss files into regular css files.

  yarn add sass-loader@6.0.6 node-sass@4.5.3

17) Add normalize.css

  yarn add normalize.css@7.0.0

  Go to node_modules and verify its path: normalize.css/normalize.css and import it to app.js;

  Addjust webpack to accept css as well.

18) Install react-router:

    Documentation: https://github.com/ReactTraining/react-router
    Documentation: https://reacttraining.com/react-router/
    Command: yarn add react-router-dom@4.2.2

    react-router-dom install all the react-router API for web apps, and not the complete API wich include react native as well (for react native, install react-router-native).
