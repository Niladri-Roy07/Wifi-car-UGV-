# 🚗 ESP32 WiFi-Controlled Car

This project allows you to control a car using an **ESP32 microcontroller** over a self-hosted WiFi network. The car can move **forward**, **backward**, **left**, **right**, or **stop**, all through a simple web interface hosted by the ESP32 itself — no internet required.

---

## 🌐 Features

- ESP32 runs in **Access Point (AP) mode**
- Onboard **web server** for motor control
- HTML UI with clickable directional buttons
- Control directions: Forward, Backward, Left, Right, Stop
- Easily expandable (e.g., camera module, speed control)

---

## 🧰 Hardware Required

- 🧠 ESP32 Dev Board  
- ⚙️ L298N Motor Driver  
- ⚡ 2 DC Motors  
- 🔋 Power Source (battery or USB)  
- 🧵 Jumper Wires & Breadboard  
- 🚗 Car chassis (optional but recommended)

---

## 📶 How It Works

1. ESP32 boots and creates a WiFi Access Point: `ESP32_Car`
2. You connect your phone/laptop to this WiFi
3. Open a browser and go to: [`http://192.168.4.1`](http://192.168.4.1)
4. Control the car via a web-based control panel

---

## 📷 Circuit Diagram

![Pin Connection Diagram](pin-diagram.png)  
*Refer to the uploaded image for exact wiring and GPIO mappings.*

---

## 🖥 Web UI

The ESP32 hosts this simple HTML page:

```html
<h1>ESP32 WiFi Car</h1>
<button onclick="location.href='/F'">Forward</button><br>
<button onclick="location.href='/L'">Left</button>
<button onclick="location.href='/S'">Stop</button>
<button onclick="location.href='/R'">Right</button><br>
<button onclick="location.href='/B'">Backward</button>
