# WebRTC Media Stream Communication

This project demonstrates how peer-to-peer video and audio communication works using WebRTC.

## Key Concepts

### 📹 Media Stream Negotiation

We use the addTrack() method to add audio and video tracks from the local media stream to the peer connection. These tracks are exchanged between peers during the offer/answer process so both sides can agree on a common media format.

### 🔁 Bi-Directional Communication

By adding local tracks to the connection, both peers can send and receive audio and video. This allows real-time two-way communication — your stream goes to the other peer, and their stream is played back locally.

### 🎛 Codec Negotiation

When tracks are added, WebRTC automatically negotiates the best supported audio and video codecs between the two peers. This ensures smooth playback and good media quality.

### 🌐 ICE Candidate Exchange

Adding tracks triggers ICE (Interactive Connectivity Establishment) candidate gathering. ICE helps peers connect directly, even if they’re behind NAT or firewalls, by finding the best network path.

### 📡 Signaling

After adding tracks, we update the peer connection’s local description. This contains info about media and ICE candidates, which we send to the remote peer via a signaling channel (e.g., WebSocket, Firebase, etc.) to complete the connection setup.

---

## How to Run

1. Clone the repository
2. Start a local web server (e.g. npx serve)
3. Open the app in two browser tabs or devices
4. Follow the UI to initiate a video/audio call

---

## Technologies Used

- WebRTC
- JavaScript
- HTML/CSS
- Signaling (custom)

---

## License

This project is for educational/demo purposes.
