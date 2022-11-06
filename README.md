WebRTC based video chat app whose name and other stuff is 100% orignal.
I would write some sexy and sophisticated line, but I have lost it.

# [Demo](https://mooz-app.netlify.app/)

TODO A good-looking gif

# Uses

- **`React`** my love.
- **`Socketio`** for signaling and room management. I don't use `REST` and `Express` at all in this, sue me.
- **`Fluentui`** for good-looking UI components without writing much CSS and therefore less hairfall.
- **`Recoil`** for local state management, fuck `Redux`.

Pretty known thing for peer-to-peer WebRTC connections but I will still state this for commercial purposes: 
All connection data like video, audio and messages are tranfered peer to peer without going through server.

# Goal

Open source peer-to-peer video conferencing app core, easily deployable and extendable for custom use cases. So instead of everyone creating those ugly video chat apps, this can be extended for any extra custom features like, file sharing, session recording, options for Media server based solution and/or encryption, etc.

# Limitations

It scales very well in terms of how many rooms can be on server as it is a peer to peer solution, infact a peer doesn't even need to be connected to server once connection is esablished with other peer. However there is a huge natural limitation on how many participants can be in one single room due to bandwidth and processing requirements. Peer-to-peer playes negative role on that front as every peer is sending and recieving data with every peer in a room. This limitation is little overcomed with adaptive bandwidth usage and other optimizations, but core limitation is by design.

# Why node-cache instead of database?

Works for now