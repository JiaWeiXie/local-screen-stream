# Local Stream


## Stream Media Server

- [MediaMTX](https://github.com/bluenviron/mediamtx?tab=readme-ov-file#installation)

1. edit `.env.example` to `.env`
```
MTX_WEBRTCADDITIONALHOSTS=local network ip ex: 192.168.x.x
```
2. docker compose up -d


## OBS

OBS Studio

OBS Studio can publish to the server in multiple ways (SRT client, RTMP client, WebRTC client). The recommended one consists in publishing as a RTMP client. In Settings -> Stream (or in the Auto-configuration Wizard), use the following parameters:

- Service: Custom...
- Server: rtmp://localhost
- Stream key: mystream

Save the configuration and click Start streaming.


## Client

### VLC Media Player

- File -> Open Network
- Paste URL:
`rtsp://<local-network-ip>:8554/mystream`
