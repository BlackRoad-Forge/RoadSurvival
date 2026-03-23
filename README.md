# RoadSurvival

> Offline AI survival expert — Pi 5 + Hailo-8

Part of the [BlackRoad OS](https://blackroad.io) ecosystem — 18 orgs, 20 domains, 200 agents.

Forked from [`thotsl4yer69/survival-companion`](https://github.com/thotsl4yer69/survival-companion) and enhanced for the BlackRoad sovereign stack.

| | |
|---|---|
| **Language** | Multiple |
| **Organization** | [BlackRoad-Forge](https://github.com/BlackRoad-Forge) |
| **License** | See upstream |
| **Homepage** | [blackroad.io](https://blackroad.io) |

---

# Survival Companion

**Offline AI survival expert system for Raspberry Pi 5 with Hailo-8 accelerator**

[![Status](https://img.shields.io/badge/status-deployed-success)](http://192.168.1.219:5000)
[![Features](https://img.shields.io/badge/features-260%2F260-brightgreen)](./api/features.db)
[![Production](https://img.shields.io/badge/production-25%25-yellow)](./DEPLOYMENT_STATUS.md)
[![License](https://img.shields.io/badge/license-MIT-blue)](./LICENSE)

> 🚨 **Critical Update:** All fake/simulated data has been removed. System now returns truthful "not available" messages when sensors aren't connected.

---

## Overview

An autonomous survival companion providing:
- 🏥 **Medical AI** - 12 first aid protocols with step-by-step guidance
- 🗺️ **GPS Navigation** - Waypoints, breadcrumb trails, position tracking
- 🌤️ **Weather Monitoring** - Real-time environmental data and storm alerts
- 👁️ **Vision AI** - Plant/animal identification, wound assessment, skin screening
- 📊 **Vitals Monitoring** - SpO2, heart rate, body temperature tracking
- 🚨 **Emergency SOS** - Audio beacon, position broadcast, emergency info
- 🎤 **Voice Interface** - Wake word activation, natural language queries
- 🧠 **Dual LLM System** - Phi-3 (general) + BioMistral (medical) queries

**Built for:** Remote wilderness survival, disaster scenarios, off-grid medical support

---

## Quick Start

### Access Web Dashboard

http://192.168.1.219:5000

**Available now:**
- ✅ Medical protocols (12 first aid guides)
- ✅ System status and configuration
- ✅ API endpoints (100+)
- ⚠️ Sensor data (shows "not available" - hardware pending)

### Hardware Requirements

**Minimum System (~$55-75):**
- Raspberry Pi 5 (16GB RAM recommended)
- BME280 sensor (weather) - $5-10
- GPS NEO-6M module - $15-25
- Camera OV5647/IMX219 - $15-30
- ili9486 TFT display (3.5-5") - $20-40

**Full System (~$80-100):**
- Add MAX30102 (vitals) - $8-15
- Add MLX90614 (temperature) - $15-25
- Add Piezo buzzer (SOS) - $2-5

**AI Accelerator:**
- Hailo-8 (26 TOPS) - Optional but recommended for vision AI

---

## Documentation

**Essential Guides:**
- [API Reference](./API_REFERENCE.md) - All 100+ endpoints
- [Deployment Status](./DEPLOYMENT_STATUS.md) - Current progress (25%)
- [Hardware Setup](./HARDWARE_SETUP_GUIDE.md) - Complete wiring diagrams
- [Hardware FAQ](./HARDWARE_FAQ.md) - Sensor requirements, Hailo usage
- [Session 53 Summary](./SESSION_53_SUMMARY.md) - Latest deployment

---

## API Examples

### Get Medical Protocol

```bash
# List all protocols
curl http://192.168.1.219:5000/api/protocols

# Get specific protocol (CPR)
curl http://192.168.1.219:5000/api/protocols/12 | json_pp
```

### Check Vitals (requires sensors)

```bash
curl http://192.168.1.219:5000/api/vitals/current
# Returns: {"error": "SENSORS_NOT_AVAILABLE"} until hardware connected
```

### GPS Position (requires GPS)

```bash
curl http://192.168.1.219:5000/api/gps/position
# Returns: {"error": "GPS_NOT_AVAILABLE"} until GPS connected
```

See [API_REFERENCE.md](./API_REFERENCE.md) for complete documentation.

---

## Current Status

**Deployment Phase:** 1 of 4 (Software Deployment)

**Production Readiness:** 25% (3/12 milestones)

- ✅ Application deployed to Pi5
- ✅ Hailo-8 drivers installed
- ✅ All fake data removed
- 🔴 Physical sensors (0/7 connected)
- 🔴 Display configured
- 🔴 Vision models compiled (.hef)

**Next:** Connect physical sensors and verify real data collection.

See [DEPLOYMENT_STATUS.md](./DEPLOYMENT_STATUS.md) for complete checklist.

---

## License

MIT License

---

## Contact

**Repository:** https://github.com/thotsl4yer69/survival-companion

**Live Demo:** http://192.168.1.219:5000 (local network only)

---

**Status:** Deployed - Awaiting Hardware Assembly 🚀

**Last Updated:** 2026-01-16
