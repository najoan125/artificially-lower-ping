# Minecraft Redirect Proxy
This is a project that allows users to setup a proxy where any minecraft client can connect to any remote host. This project would be useful for individuals who want to hide their IP address using a remote server, or possibly allowing an extra layer of filtering for server administrators. 
## Usage
Download from [releases](https://github.com/sugoidogo/minecraft-redirect-proxy/releases/latest).
On first run, the default config given below will be written and used.
Run the jar and edit config.json accordingly.

## Configuration
```
{
  "versionName": "ProxyCup",
  "maxPlayers": 1337,
  "onlinePlayers": 133,
  "motd": "Couldnt connect to requested backend server. If you believe this to be an issue, contact the administrator of this proxy.",
  "port": 22000,
  "nodes": [
    {
      "hostname": "localhost",
      "remoteHostname": "mc.hypixel.net",
      "remoteHostPort": 25565
    },
    {
      "hostname": "127.0.0.1",
      "remoteHostname": "mc.arkhamnetwork.org",
      "remoteHostPort": 25565
    }
  ]
}
```

| Option | Info | Type |
|-|-|-|
| versionName | The custom version name if connecting to backend server fails | String |
| maxPlayers | Max players if connecting to backend server fails. | Integer |
| onlinePlayers | Online players if connecting to backend server fails.| Integer |
| motd | MOTD of server if connecting to backend server fails. | String |
| port | Port that the proxy server should listen on. | Integer |
| nodes | An array of nodes which specify how to redirect requests based on the hostname of the server the client is trying to connect to. | Array |
| hostname | the hostname or ip requested by the client | String |
| remoteHostname | the hostname or ip to proxy the connection to | String |
| remoteHostPort | the port on the remote host to proxy the connection to | Integer |