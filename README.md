# Docker VueJS dev environment

## Usage

1) Run containers from `compose` directory: `docker-compose up -d --build --remove-orphans`
2) Application will be synced to `app` directory
3) Access container's terminal: `docker-compose exec vue bash`
4) Create new VueJS Webpack project: `vue init webpack my-project`
5) Change host to access app running in Docker container:
```js
module.exports = {
  dev: {
    //host: 'localhost', // change to
    host: '0.0.0.0',
    ...
  }
}
```
6) Run `npm run dev` to serve an app
7) Go to `localhost:8080` in your browser