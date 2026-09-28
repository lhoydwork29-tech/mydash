# mydash

## Run the dashboard

Install Node.js, then start the dashboard server from this folder:

```sh
npm start
```

Open `http://localhost:3000` to use the dashboard. The Node server is the source of truth and saves changes in `data/dashboard-state.json`; it loads the latest saved data whenever the dashboard opens. Keep this server running and use its address from every browser or device that should access the same dashboard. For another device on the same network, use `http://<computer-LAN-IP>:3000` and allow network access to port `3000`.

The server sends updates to other open dashboard sessions and rejects saves based on an outdated version, so one device cannot silently overwrite newer server data. To keep data across server restarts or deployments, retain the `data` directory on persistent storage.