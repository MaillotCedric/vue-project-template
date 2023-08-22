# Project template : Vue

Template for Vue projects.

The template is based on Vue.js and allows you to rapidly create a front-end web app.

This template uses [Vuetify](https://vuetifyjs.com/en/).

> Vuetify : a collection of pre-made components paired with powerful features

## Setting up the repository

- Choose a new repository name

- Use it to rename the current cloned repository

- Delete the current `.git` folder (the folder might be hidden)

- Update `README.md`

- Run the following command in the terminal of the repository :

  ```git
  git init
  git add .
  git commit -m "<commit message>"
  ```

*You are now ready to install the project. :)*

## Installation

``` powershell
npm install
npm run format
```

### Compile and Hot-Reload for Development

``` powershell
npm run dev
```

## Compile and Minify for Production

``` powershell
npm run build
```

## Run Unit Tests with [Vitest](https://vitest.dev/)

``` powershell
npm run test:unit
```

## Run End-to-End Tests with [Cypress](https://www.cypress.io/)

``` powershell
npm run test:e2e:dev
```

This runs the end-to-end tests against the Vite development server. It is much faster than the production build.

But it's still recommended to test the production build with `test:e2e` before deploying (e.g. in CI environments) :

``` powershell
npm run build
npm run test:e2e
```

## Lint with [ESLint](https://eslint.org/)

``` powershell
npm run lint
```

## Quick installation

For a quick and easy installation we using **Docker**, so make sure you have Docker installed.

> [How to install and use Docker](https://docs.docker.com/)

### Containerize the application

Run the following command in the terminal of the repository :

```bash
docker compose up -d --build
```

### Access the application

Now that we have our container up and running, we can easily access the application by opening our favorite browser to http://localhost:5173

## Update the application

Since our application is containerized, when you update the application, you are gonna have to rebuild the Docker container to see the effective updates.

You can rebuild the container by running the following commands in the terminal of the repository :

```bash
# rebuild the container
docker compose up -d --build
# remove old images
docker image prune
```

## Stop the container

You can stop the container by running the following command in the terminal of the repository :

```bash
docker compose stop
```

> When stopping the container, the application is not accessible anymore.
>
> To access the application again, you are gonna have to restart the container.

You can restart the container by running the following command in the terminal of the repository :

```bash
docker compose start
```
## Share the application

To share the application, we have to use a Docker registry.

The default registry is Docker Hub.

> [More information on how to share an app](https://docs.docker.com/get-started/04_sharing_app/)

### Push on Hub

Run the following commands in the terminal of the repository :

```bash
docker build -t YOUR-USER-NAME/vue-project-template-app .
# if you are not logged in
docker login
docker push YOUR-USER-NAME/vue-project-template-app
```

### Update on Hub

Run the following commands in the terminal of the repository :

```bash
docker build -t YOUR-USER-NAME/vue-project-template-app .
docker image prune
# if you are not logged in
docker login
docker push YOUR-USER-NAME/vue-project-template-app
```
