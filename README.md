# React Webpack Babel Starter

Minimal starter kit with hot module replacement (HMR) for rapid development.

- **[React](https://facebook.github.io/react/)** (16.x)
- **[Webpack](https://webpack.js.org/)** (4.x)
- **[Hot Module Replacement (HMR)](https://webpack.js.org/guides/hmr-react/)** using [React Hot Loader](https://github.com/gaearon/react-hot-loader) (4.x)
- **[Babel](http://babeljs.io/)** (6.x)
- **[LESS](http://lesscss.org/)**
- [Jest](https://facebook.github.io/jest/) - Testing framework for React applications
- **Image loading/minification using [Image Loader](https://github.com/vanwagonet/img-loader)**
- Code quality (linting) for JavaScript and LESS/CSS.
- **[Redux](https://redux.js.org/)** Manage the Component states.
- **[Redux-Thunk](https://github.com/reduxjs/redux-thunk)** The middle-ware of Redux
- **[Redux-toolbelt](https://github.com/welldone-software/redux-toolbelt)** A set of tools for quicker, easier, less verbose and safer Redux development by [welldone-software](http://welldone-software.com/).
- ESLINT for Javascript and ReactJs
- JSHINT standard configuration.

* Convert CSS to LESS: http://kronus.me/cn/css2less/

# Original Source Code

The source had been clone from [vikpe/react-webpack-babel-starter](https://github.com/vikpe/react-webpack-babel-starter) and on top of that I added some useful packages includes the Finished the [Material-Dashboard-React](https://github.com/creativetimofficial/material-dashboard-react) and Redux integration

# Support Features

## 1. async/await

It is using `babel-regenerator-runtime` to transform the async and await functions to Promise.

```javascript
//Transform from
function getDataFromServer() {
  return Promise((resolve, reject) => {
    loadDataFromServer()
      .then(data => resolve(data))
      .catch(error => reject(error));
  });
}

//To
async function getDataFromServer() {
  try {
    return await loadDataFromServer();
  } catch (error) {
    throw error;
  }
}
```

## Installation

1.  Clone/download repo
2.  `npm install`

## New Compoments

1.  **Message Box and Notification**: Allow to show Info, Confirm, Success and Error message and notification. Refer to the MessageBox in Views folder so sample that using Redux store to manage the state.

## Usage

### Development

`npm run start-dev`

- Build app continously (HMR enabled)
- App served @ `http://localhost:8080`

### Production

`npm run start-prod`

- Build app once (HMR disabled)
- App served @ `http://localhost:3000`

---

### Docker Support

1.  Build Image `docker build`.
2.  Build and Tag the image `docker image build . -t [YOUR_ID]/react-materialui-started-kit:latest` exmple `docker image build . -t baoduy2412/react-materialui-started-kit:latest`.
3.  Push inage to Docker hub `docker push [YOUR_ID]/react-materialui-started-kit:latest` example `docker push baoduy2412/react-materialui-started-kit:latest`.

The application will running port 3000 in Docker.
The image can be found in Docker hub [here](https://hub.docker.com/r/baoduy2412/react-materialui-started-kit/).

### All commands

| Command              | Description                                                              |
| -------------------- | ------------------------------------------------------------------------ |
| `npm run start-dev`  | Build app continuously (HMR enabled) and serve @ `http://localhost:8080` |
| `npm run start-prod` | Build app once (HMR disabled) and serve @ `http://localhost:3000`        |
| `npm run build`      | Build app to `/dist/`                                                    |
| `npm run test`       | Run tests                                                                |
| `npm run lint`       | Run JavaScript and LESS linter                                           |
| `npm run lint:js`    | Run JavaScript linter                                                    |
| `npm run lint:less`  | Run LESS linter                                                          |
| `npm run start`      | (alias of `npm run start-dev`)                                           |

## See also

- [React Webpack Typescript Starter](https://github.com/vikpe/react-webpack-typescript-starter)
- [Isomorphic Webapp Starter](https://github.com/vikpe/isomorphic-webapp-starter)
