# 🌸 Sakura-AI-Monitor-2

## 📌 Project Overview

Sakura AI is a Python and Flask-based network traffic monitoring dashboard designed to visualize packet flows, monitor ingress and egress network activity, and demonstrate rule-based packet analysis using simulated network traffic.

The project combines Flask back-end processing with an interactive front-end dashboard to demonstrate concepts commonly found in Security Operations Center (SOC) environments. Through dynamic visualizations and telemetry displays, Sakura AI provides an educational platform for exploring network monitoring, packet analysis, and secure application development.

> **Project Status:** 🚧 Development Paused (Application Security Case Study)

---

## ⚙️ Core Architecture & Flow

The application runs on a local Flask server (`http://127.0.0.1:5000/`) and follows a four-stage processing pipeline:

### 1. Ingestion
- Flask routes load simulated network traffic from a sandboxed dataset.
- Represents inbound and outbound network communication for analysis.

### 2. Extraction
The application parses key packet metadata, including:

- Source IP Address
- Destination IP Address
- Network Protocol
- Packet Length (Bytes)

### 3. Classification
Packet attributes are evaluated against predefined thresholds to identify potentially suspicious activity, such as unusually large packet sizes.

### 4. Visualization
Jinja templates dynamically render packet telemetry, dashboard statistics, and interactive visualizations, including:

- Network Statistics
- Packet Telemetry Table
- Traffic Visualization
- Threat Severity Indicator
- Network Topology
- Activity Feed
- AI Analysis Panel

---

## 🔒 Security Context & Data Privacy

The application is developed using **synthetic network traffic** to protect sensitive information while demonstrating cybersecurity monitoring concepts.

### Local Development
The application runs on the local loopback interface (`127.0.0.1`) during development, preventing external access unless explicitly configured.

### Synthetic Baseline Testing
A sandboxed dataset of simulated IPv4 addresses is used to model realistic network communication without exposing production infrastructure.

### Network Segment Mapping
The dashboard models communication between simulated private RFC 1918 address space (`10.0.0.x`) and mock external endpoints to demonstrate internal and external network traffic patterns.

### Rule-Based Detection
Packets that exceed predefined thresholds are highlighted to demonstrate how security dashboards can identify potentially suspicious activity.

Example:

> **Suspicious:** Unusually large packet detected (Packet Length: 264 bytes)

---

## 🛡️ Planned Security Enhancements

Development of new features has been paused while the repository is documented as an **Application Security (AppSec) case study**. Planned improvements include:

### Input Validation & Sanitization
- Validate incoming packet data
- Sanitize user-controlled input
- Reduce the risk of Cross-Site Scripting (XSS)

### Flask Security Configuration
- Disable `debug=True` in production
- Implement secure environment variable management
- Improve production deployment configuration

### Content Security Policy (CSP)
- Configure secure HTTP response headers
- Restrict inline script execution
- Reduce client-side attack surface

### Role-Based Access Control (RBAC)
- User authentication
- Role-based authorization
- Protected administrative functionality

### Secure Communication
- HTTPS/TLS support
- Secure session management
- Secure cookie configuration

### Monitoring & Logging
- Security event logging
- Audit trail generation
- Automated alerting

---

## 💻 Technologies

### Backend
- Python
- Flask
- Pandas

### Frontend
- HTML5
- CSS3
- JavaScript
- Jinja2
- Chart.js

### Development Tools
- PyCharm
- Git
- GitHub

---

## 🎯 Skills Demonstrated

This project demonstrates experience with:

- Python application development
- Flask web framework
- HTML, CSS, and JavaScript
- Jinja templating
- Dashboard UI/UX design
- Network traffic visualization
- Packet metadata analysis
- Cybersecurity monitoring concepts
- Application Security (AppSec) fundamentals
- Git version control and documentation

---

## 🚀 Future Roadmap

Planned enhancements include:

- Real-time packet capture using Scapy
- Machine learning-assisted anomaly detection
- Interactive network topology improvements
- Historical traffic analytics
- Database integration
- Exportable security reports
- Live WebSocket updates
- Enhanced AI-assisted analysis

---

## 📄 Disclaimer

Sakura AI is an educational and portfolio project created to demonstrate cybersecurity monitoring concepts, Flask web development, and secure software engineering practices.

All packet data, IP addresses, and network activity displayed within the application are synthetic and used solely for development, testing, and educational purposes.
