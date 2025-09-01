# 🌐 Browser Web APIs Cheat Sheet

This sheet lists **important Web APIs** provided by browsers with **1-line explanation + example**.  
Great for **interview prep + quick revision**.

---

## 1. DOM & Document APIs
- **DOM API** → Access/manipulate HTML elements.  
  `document.getElementById("myDiv").innerText = "Hello!";`

- **CSSOM API** → Change CSS styles dynamically.  
  `document.getElementById("myDiv").style.color = "red";`

- **Geolocation API** → Get user’s location.  
  `navigator.geolocation.getCurrentPosition(p => console.log(p.coords));`

- **Selection API** → Work with selected text.  
  `console.log(window.getSelection().toString());`

- **Fullscreen API** → Enter fullscreen mode.  
  `document.documentElement.requestFullscreen();`

---

## 2. Event Handling APIs
- **EventTarget API** → Add/remove event listeners.  
  `btn.addEventListener("click", () => alert("Clicked!"));`

- **Pointer Events API** → Handle mouse/touch/pen input.  
  `document.addEventListener("pointerdown", e => console.log(e.pointerType));`

- **Drag & Drop API** → Enable drag-and-drop UI.  
  `drag.ondragstart = e => e.dataTransfer.setData("text", "Dragged!");`

- **Clipboard API** → Copy/paste to clipboard.  
  `navigator.clipboard.writeText("Copied!");`

---

## 3. Timers & Scheduling
- **Timers API** → Run code later or repeatedly.  
  `setTimeout(() => console.log("After 2s"), 2000);`

- **Animation Frame API** → Smooth animations.  
  `requestAnimationFrame(() => console.log("Frame!"));`

---

## 4. Networking APIs
- **Fetch API** → Make HTTP requests.  
  `fetch("/data.json").then(r => r.json()).then(console.log);`

- **XMLHttpRequest (XHR)** → Old way to fetch data.  
  `let xhr = new XMLHttpRequest(); xhr.open("GET", "/data"); xhr.send();`

- **WebSocket API** → Real-time communication.  
  `let ws = new WebSocket("wss://echo.websocket.org");`

- **Server-Sent Events (SSE)** → Receive live updates.  
  `let es = new EventSource("/events"); es.onmessage = e => console.log(e.data);`

---

## 5. Storage & Data APIs
- **LocalStorage API** → Save key/value permanently.  
  `localStorage.setItem("name", "Sathvik");`

- **SessionStorage API** → Save data for session only.  
  `sessionStorage.setItem("x", "123");`

- **IndexedDB API** → Store structured data offline.  
  `indexedDB.open("myDB", 1);`

- **Cookies** → Store small key/value in browser.  
  `document.cookie = "username=Sathvik";`

---

## 6. Multimedia APIs
- **HTMLMediaElement API** → Control video/audio.  
  `document.getElementById("video").play();`

- **Canvas API** → Draw 2D graphics.  
  `ctx.fillRect(20,20,100,100);`

- **Web Audio API** → Process/play sound.  
  `new AudioContext().createOscillator().start();`

- **Media Capture API** → Access camera/mic.  
  `navigator.mediaDevices.getUserMedia({ video: true });`

- **WebRTC API** → Peer-to-peer audio/video chat.  
  `new RTCPeerConnection();`

---

## 7. Graphics & Animation APIs
- **Canvas API** → Draw graphics.  
  `ctx.fillRect(50,50,80,80);`

- **WebGL API** → 3D graphics rendering.  
  `canvas.getContext("webgl");`

- **SVG API** → Work with SVG elements.  
  `<circle cx="50" cy="50" r="40" fill="green"/>`

- **Animation API** → Animate elements.  
  `box.animate([{transform:"translateX(0)"},{transform:"100px"}], {duration:1000});`

---

## 8. Device APIs
- **Geolocation API** → Get user’s location.  
  `navigator.geolocation.getCurrentPosition(p => console.log(p.coords));`

- **Battery Status API** → Battery info (deprecated).  
  `navigator.getBattery().then(b => console.log(b.level));`

- **Device Orientation API** → Detect tilt/rotation.  
  `window.addEventListener("deviceorientation", e => console.log(e.alpha));`

- **Vibration API** → Vibrate device.  
  `navigator.vibrate(500);`

- **Gamepad API** → Connect game controllers.  
  `window.addEventListener("gamepadconnected", e => console.log(e.gamepad.id));`

- **Screen Orientation API** → Get screen orientation.  
  `console.log(screen.orientation.type);`

---

## 9. Background & Workers
- **Web Workers API** → Run background threads.  
  `let w = new Worker("worker.js");`

- **Service Workers API** → Offline caching, push.  
  `navigator.serviceWorker.register("/sw.js");`

- **Push API** → Receive push notifications.  
  `Notification.requestPermission();`

- **Background Sync API** → Retry tasks offline.  
  *(Used with Service Worker)*

---

## 10. Other Useful APIs
- **History API** → Control browser history.  
  `history.pushState({}, "", "/new");`

- **URL API** → Parse/manipulate URLs.  
  `new URL("https://example.com?x=1");`

- **File API** → Work with uploaded files.  
  `fileInput.onchange = e => console.log(e.target.files[0]);`

- **Notification API** → Show desktop notifications.  
  `new Notification("Hello!");`

- **Performance API** → Measure performance.  
  `console.log(performance.now());`

- **Web Crypto API** → Secure crypto operations.  
  `crypto.subtle.digest("SHA-256", new TextEncoder().encode("hi"));`

- **Payment Request API** → Handle payments.  
  `new PaymentRequest([], { total: { label:"Total", amount:{currency:"USD", value:"10.00"}}});`

- **Web Share API** → Share content to apps.  
  `navigator.share({title:"Hi", url:"https://example.com"});`

---

✅ **Interview Note**:  
Not all are equally important. Focus on these for interviews:  
- DOM & Event APIs (`getElementById`, `addEventListener`)  
- Timers (`setTimeout`)  
- Fetch API (AJAX calls)  
- Storage APIs (localStorage, cookies)  
- History & URL API  
- Basic Multimedia (Canvas, Media)  
- Web Workers & Service Workers (optional, for PWA roles)  

---
