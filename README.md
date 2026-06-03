# ⚡ Elektrum - Home Energy Dashboard

**Where Energy Meets Intelligence**

Real-time energy monitoring system with predictive analytics, room-wise consumption tracking, and smart billing integration for Sri Lankan homes.

---

## ✨ Key Features

### 📊 Real-Time Monitoring
- Live power consumption tracking (Watts)
- Voltage and current monitoring
- Temperature & humidity sensors
- 5-second data refresh intervals
- 24-hour historical data

### 🏠 Room-Wise Analytics
- Individual room power consumption tracking
- Current (Amperes) and power (Watts) breakdown
- Average and peak power metrics
- Visual power distribution pie charts
- Room-specific consumption percentages

### 🤖 Predictive Analytics
- Ridge Regression time-series forecasting
- Consumption pattern analysis
- Daily/weekly/monthly trend predictions
- Real-time model status indicator

### 💡 Smart Reports & Billing
- **PDF Report Generation**: Weekly and monthly summaries
- **Bill Integration**: Quick links to CEB and LECO payment portals
- **Cost Estimation**: Daily, monthly cost calculations (₹13.06/kWh default)
- **Carbon Tracking**: Monthly CO₂ footprint calculations in kg

### 📈 Visualizations
- 24-hour usage pattern charts
- Power consumption by room (bar charts)
- Power distribution pie charts
- System status monitoring
- Real-time data points counter

### 🔌 Connected Systems
- MongoDB for historical data storage
- IoT sensor integration
- Active connection status indicator
- Scalable architecture

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React, Tailwind CSS, Chart.js |
| **Backend** | FastAPI, Python |
| **Database** | MongoDB |
| **IoT/Sensors** | Real-time energy sensors |
| **Data Processing** | Ridge Regression, Time-series analysis |
| **Deployment** | Vercel & AWS EC2 |

---

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- Python 3.9+
- MongoDB instance
- IoT energy sensors/smart meters

### Frontend Setup
```bash
# Install dependencies
npm install

# Start development server
npm start

# Build for production
npm run build
```

### Backend Setup
```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start FastAPI server
uvicorn main:app --reload
```

### Environment Variables
```env
# Frontend (.env)
REACT_APP_API_URL=http://localhost:8000

# Backend (.env)
MONGODB_URI=mongodb://localhost:27017
DATABASE_NAME=elektrum
SENSOR_UPDATE_INTERVAL=5
```

---

## 📋 Project Structure

```
elektrum/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Dashboard.jsx
│   │   │   ├── RoomConsumption.jsx
│   │   │   ├── Charts.jsx
│   │   │   └── BillPayment.jsx
│   │   ├── pages/
│   │   └── App.jsx
│   └── package.json
├── backend/
│   ├── main.py
│   ├── models/
│   │   ├── sensor.py
│   │   └── room.py
│   ├── routes/
│   │   ├── energy.py
│   │   ├── analytics.py
│   │   └── reports.py
│   ├── services/
│   │   ├── prediction.py
│   │   └── pdf_generator.py
│   └── requirements.txt
└── README.md
```

---

## 🎮 Usage

### View Real-Time Metrics
- Dashboard displays live power consumption, voltage, temperature, and humidity
- Auto-refreshes every 5 seconds
- Filter data by time range (1h, 6h, 24h, 7d)

### Monitor Room Consumption
- Check individual room power usage
- Compare current, average, and peak consumption
- Identify high-usage rooms instantly

### Generate Reports
- Click "Weekly Report" or "Monthly Report"
- Includes consumption breakdown, daily stats, costs, and carbon footprint
- PDFs ready for download

### Pay Bills
- Quick links to CEB (Ceylon Electricity Board) and LECO payment portals
- Estimated monthly bill based on consumption
- Accurate rate calculations

---

## 📊 Predictions & Analytics

The system uses **Ridge Regression** for time-series forecasting:
- Analyzes historical consumption patterns
- Predicts future energy usage
- Helps identify optimization opportunities
- Real-time model status display

---

## 🌍 Sri Lanka Specific Features

- **Billing Integration**: Direct links to CEB and LECO portals
- **Local Pricing**: Default rate ₹13.06/kWh (configurable)
- **Carbon Footprint**: Monthly CO₂ tracking in kg
- **Multi-Language Support**: Ready for Sinhala/Tamil translation

---

## 📈 API Endpoints

### Energy Data
- `GET /api/energy/current` - Current power metrics
- `GET /api/energy/history?room=&range=24h` - Historical data
- `POST /api/energy/log` - Log sensor reading

### Analytics
- `GET /api/analytics/predict?days=7` - Predict next 7 days
- `GET /api/analytics/patterns` - Get consumption patterns
- `GET /api/analytics/carbon-footprint` - Monthly CO₂ data

### Reports
- `POST /api/reports/generate?type=weekly` - Generate PDF
- `GET /api/reports/estimated-bill` - Calculate estimated cost

---

## 🔮 Future Enhancements

- [ ] Smart device integration (IoT appliance control)
- [ ] Mobile app (React Native/Flutter)
- [ ] Machine learning optimization suggestions
- [ ] Solar panel integration & off-grid monitoring
- [ ] Automated alerts for peak usage
- [ ] Multi-home support
- [ ] Advanced anomaly detection
- [ ] Dark mode UI

---

## 📝 License

MIT License - Feel free to use, modify, and distribute

---

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📧 Contact & Support

- **Issues**: Open a GitHub issue for bugs and feature requests
- **Email**: kavix@yahoo.com
- **Live Demo**: https://cd-kavindu.vercel.app/

---

## 🎯 Status

🚀 **Active Development** - v1.0.0 Released

- ✅ Core dashboard functionality
- ✅ Room-wise monitoring
- ✅ Predictive analytics
- ✅ PDF report generation
- ⏳ Mobile app in progress
- ⏳ Advanced ML features

---

**⚡ Monitor. Predict. Optimize. Save.**
