Run containers from `compose` directory:

`docker-compose up -d --build --remove-orphans`

Application will be synced to `app` directory

Access container's terminal:

`docker-compose exec vue bash`

Create new VueJS Webpack project:

`vue init webpack my-project`

Change host to access app running in Docker container:

```js
module.exports = {
  dev: {
    //host: 'localhost', // change to
    host: '0.0.0.0',
    ...
  }
}
```
Run `npm run dev` to serve an app