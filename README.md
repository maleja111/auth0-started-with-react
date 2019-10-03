This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Step # 1: Setup a React App

```npx create-react-app auth0-started-with-react```
```cd auth0-started-with-react```
```npm start```

## Step # 2: Navigation in our app

```npm i react-router react-router-dom```
Update `index.js`
```jsx
// other imports
import { BrowserRouter } from 'react-router-dom';
ReactDOM.render(
  <BrowserRouter>
    <App />
  </BrowserRouter>,
  document.getElementById("root")
);
serviceWorker.unregister();
```

## Step # 3: Configure an application on Auth0.com

Allowed Callback URLs: `http://localhost:3000/callback`
Allowed Web Origings: `http://localhost:3000`
Allowed Logout URLs: `http://localhost:3000`

## Step # 4: Secure React App with Auth0

```npm install auth0-js```
Create a new file `Callback.js` inside `src`
Link: File

## Step # 5: Fetch the user information sent by Auth0

```npm install auth0-js```
Create a new file `Auth.js` inside `src`
Link: File

## Step # 6: Some changes in App
Update our `App.js`.
Link: File
Create a new file `Home.js` inside `src`
Link: File

## Final step: `npm start`

## Optional: Deploy to Heroku

Let's create our app in Heroku:

``` sh
heroku create <app-name> --buildpack mars/create-react-app
```

This will create an app on https://<app-name>.herokuapp.com, make sure to update `Auth.js` redirect uri with this value.

The you'll need to change your code to use environment variables
- Update `Auth.js` to use:
  * `process.env.REACT_APP_AUTH0_DOMAIN`
  * `process.env.REACT_APP_AUTH0_CLIENT_ID`

And create those environment variables in Heroku:

``` sh
heroku config:set REACT_APP_AUTH0_DOMAIN=<domain>
heroku config:set REACT_APP_AUTH0_CLIENT_ID=<client-id>
```

Then, add the uptaded files to git, commit and then deploy by pushing to `heroku master`:

```
git push heroku master
```

# Other Info

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Credits

Get Started with Auth0 Video Series [Documentation](https://auth0.com/docs/videos/get-started) Bobby Johnson.
React Tutorial: Building and Securing Your First App [Documentation](https://auth0.com/blog/react-tutorial-building-and-securing-your-first-app) Bruno Krebs.
Start React with Auth0 [Documentation](https://medium.com/@saurssaurav33/start-react-with-auth0-107525cb969) Saurs Sauravn.

### slides
[Slides](https://docs.google.com/presentation/d/1yN03vvyhP3lw7SxrfsmJuOa5785Cm0HMcrirGnwtg4U/edit?usp=sharing)

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
