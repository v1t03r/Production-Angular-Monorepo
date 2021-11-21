# Angular Production

![Angular Production App](apps/dashboard/src/assets/screenshots/app.png)

The sample project includes an Angular web application and a mock RESTful API  within an Nx workspace by NRWL. The Angular application uses state and data libs to manage state and handle server communication. The state lib is built around NgRx and the application is entirely reactive. 

## Web: Getting Started

```
git clone https://github.com/v1t03r/Production-Angular-Monorepo.git
cd fem-production-angular
yarn
npm run serve:all
```

The `serve:all` command is a convenience methods that runs the `serve:api` and `serve:web` commands concurrently. You can run each command separately if you need to.

```
"serve:api": "nx run api:serve",
"serve:web": "ng serve --open",
"serve:all": "concurrently \"npm run serve:api\" \"npm run serve:web\""
```

The web application will open to [http://localhost:4200](http://localhost:4200) in your browser.

![Angular Production Api](apps/dashboard/src/assets/screenshots/api.png)

You can see the API by navigating to [http://localhost:3333/api/](http://localhost:3333/api/) in your browser.

> Note: the above terminal commands are for Mac. Remember to substitute the appropriate commands for your OS.

## Web: Running E2E

Because Cypress ships with Nx, E2E tests can be run with the command below.

```
npm run e2e
```

You can have Cypress watch and restart tests on test file changes with this command.

```
nx run dashboard-e2e:e2e --watch
```
