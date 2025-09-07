# Virtual Solar IoT Environment

> Simulates a virtual IoT sensor network for a **solar power plant environment** (using Python) and visualizes the data through a **Node-RED dashboard**. Developed as part of a Semester 6B IoT systems course.

---

##  Project Structure

- **Python Scripts**
  - `group06w_script.py`: Sensor simulation and MQTT publisher.
  - `group06w_thread.py`: Threaded sensor behavior for realistic data flows.
- **Node-RED Dashboard**
  - `group06w_NodeRed.json`: Dashboard flow configuration to visualize sensor data.
- **Documentation**
  - `IN18_Course_Project.pdf`
  - `IN18_IOT_network_Assignment_task2.pdf`
  - `group06w_legend.docx` / `task_02L_legend.pdf`: Legend/explanation for Node-RED elements or data interpretation.

---

##  Features

- Emulates virtual sensors (e.g., temperature, humidity, irradiance) publishing data via MQTT.
- Threaded simulation for simultaneous multi-sensor data streams.
- Node-RED dashboard for live visualization using gauges, charts, and indicators.
- Modular setup adaptable to different environments (e.g., manufacturing, solar PV systems).

---

##  Requirements

### Python (Sensor Simulation)
- Python 3.7 or higher
- `paho-mqtt` library

Install via:
```bash
pip install paho-mqtt
```

### Node-RED (Dashboard)

- Node.js + Node-RED installed (e.g., on a Raspberry Pi or local machine)
- MQTT broker (local or cloud-based)

---

## Usage
### 1. Run the Sensor Simulator

Update MQTT broker details in `group06w_script.py`, e.g.:

```python
broker = "mqtt.yourbroker.com"
port = 1883
username = "your_username"
password = "your_password"
```

Run the simulator:

```bash
python group06w_script.py
```

### 2. Deploy the Node-RED Dashboard

- Import `group06w_NodeRed.json` into your Node-RED editor.
- Configure MQTT connection nodes to match your MQTT broker settings.
- Deploy and access the dashboard, usually at:

```arduino
http://<your-host>:1880/ui
```

---

## Credits
- Developed as part of Semester 6B IoT Coursework.
- Original materials and flow structure based on course PDFs (`IN18_Course_Project.pdf`, `IN18_IOT_network_Assignment_task2.pdf`).

---
  
