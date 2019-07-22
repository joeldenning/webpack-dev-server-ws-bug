# webpack-dev-server-ws-bug

Instructions:
```sh
cd app
npm i
npm start

# new terminal tab
cd root-html
npm i
npm start
```
Now open the root-html file in a browser tab, which is usually http://localhost:5000

Notice how you'll get failed requests to http://localhost/info. The requests *should* be to
http://localhost:8080/info. Note that if you change the `start` command in `app` to specify
`--port 8080`, that the problem is fixed. In other words, the problem only exists when you
don't explicitly specify a port via webpack config or CLI, and let nodejs find a port for you.
