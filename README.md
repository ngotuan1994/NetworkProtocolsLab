# Interactive Network & Threat Simulator 🌐🛡️

An educational, interactive network simulator built entirely with vanilla JavaScript and the HTML5 Canvas API. Designed for CCNA and cybersecurity students, this visualizer demonstrates the real-time, packet-by-packet mechanics of core routing and switching protocols, as well as common Layer 2/Layer 3 network attacks.

## ✨ Features

* **Real-Time Canvas Animation:** Watch packets physically traverse links with dynamic visual feedback for drops, loops, and floods.
* **Threat Lab (Offensive Security):** Visualize exactly how network attacks happen at the packet and table level, including Man-in-the-Middle (MitM) and Distributed Denial of Service (DDoS) scenarios.
* **⚡ Chaos Mode:** Click on any router or link mid-simulation to instantly "break" it, triggering dynamic, real-time recalculations for routing protocols like OSPF.
* **Step-by-Step Debugger:** A custom execution queue allows users to pause the simulation mid-flight and manually step through packet exchanges phase-by-phase.
* **Dynamic State Tables:** View real-time updates to data structures like OSPF Link State Databases (LSDB), STP Bridge Tables, and switch CAM tables.
* **Zero Dependencies:** Built purely with Vanilla JavaScript (ES6+), HTML5, and modern CSS3. No external libraries—just lightweight, high-performance code.

## 📚 Supported Simulations

### ☠️ Network Threats & Mitigations
* **ARP Spoofing / Poisoning:** Visualizes a Man-in-the-Middle attack via fake Gratuitous ARPs and the resulting cache poisoning.
* **SYN Flood (DDoS):** Demonstrates a botnet exhausting a server's TCP Control Block queue with spoofed IPs, and mitigation via SYN Cookies.
* **MAC Flooding:** Shows an attacker overflowing a switch's CAM table to force a "fail-open" hub state, exposing all broadcast traffic.

### Routing & Switching 
* **OSPF:** Dijkstra's Shortest Path First, Hello neighbor discovery, LSA flooding, and dynamic rerouting (Chaos Mode supported).
* **BGP:** TCP session establishment, OPEN/UPDATE message exchange, and path-vector routing.
* **STP:** 802.1D Spanning Tree Protocol root bridge election and loop prevention.
* **VLAN (802.1Q):** Trunk port tagging, access port stripping, and inter-VLAN routing.

### Core Services & Transport
* **TCP/IP:** The 3-way handshake, sliding windows, data transfer, and 4-way FIN teardown.
* **ARP:** Broadcast requests, unicast replies, and Gratuitous ARP cache updates.
* **DHCP:** The full DORA process (Discover, Offer, Request, Acknowledge).
* **DNS:** Recursive client queries and iterative resolver lookups.

## 🚀 Usage

Since the project has no external dependencies or build steps, you can run it instantly:

1. Clone the repository: `git clone https://github.com/yourusername/network-protocols-lab.git`
2. Open `index.html` in any modern web browser.
3. Select a protocol or threat from the top navigation bar.
4. Click **Run** for continuous execution, or **Step** to advance phase-by-phase.

## 🛠️ Architecture Notes

The simulation runs on a custom, frame-based timing engine utilizing modern JS asynchronous patterns. Protocol logic is not pre-rendered; the `simState` object calculates actual shortest paths, builds legitimate state tables, and generates dynamic execution queues based on the selected topology. 

**Author:** Eric Tuan Ngo