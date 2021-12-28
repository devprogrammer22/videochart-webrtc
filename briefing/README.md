# briefing

> Secure video chat via pure WebRTC

**Servers**

1. Frontend: The web app the user interacts with. You find it in the `app` folder. Build it via `npm run build` and put the contents of `dist` on your server. Briefing uses some tricks to have the neat `/ng` path working.

2. Signaling Server: You can use mine for the start, which is located at `wss://sig03.brie.fi`. If you want to use your own, you find the source code in the [signal](./signal/)` folder. It is a simple node.js app that just connects peers in one room by helping to establish the WebRTC connection.

3. STUN/TURN Server: You can use mine or any other for the start. STUN is required to get peer to peer connections through firewalls. TURN is used if that does not succeed. The later one can cause some server load.


```ini
VUE_APP_ROOM_URL = https://example.com/room/
VUE_APP_ROOM_PATH = /room/
```

Similar settings are available for your own signaling and STUN/TURN servers.

When you build the distribution for your website via `npm run build` these settings will be baked in.

## Author

We are a team named DevProgrammer22, I'm a project manager and backend developer located in Hong Kong.


