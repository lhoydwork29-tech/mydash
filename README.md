# mydash

## Run the dashboard

Install Node.js, then start the dashboard server from this folder:

```sh
npm start
```

Open `http://localhost:3000` in your browser. Use that same URL in other browsers on this computer. The dashboard stores its shared data in `data/dashboard-state.json`, so edits remain after refreshes and closing the browser, and are shared with other browsers connected to this server.

To use another device on the same network, open `http://<computer-LAN-IP>:3000` there instead. Keep the server running and allow network access to port `3000`. For access from outside that network, deploy the Node server somewhere reachable and configure persistent disk storage; static-only hosting and opening `index.html` directly do not provide shared persistence.