Project Title:
AI-Based Women’s Safety Hotspot Predictor
1. Introduction
This document lists all functional, non-functional, technical, and environmental requirements for building the AI-based hotspot prediction platform aimed at improving women’s safety in public transport and urban spaces.
2. Functional Requirements
2.1 User Module
Users must be able to sign in (optional for prototype).
Users must be able to submit reports containing:
Location (GPS)
Incident type (unsafe crowd, harassment, dark area, etc.)
Time of incident
Users should be able to view:
Safety heatmap of the city
Risk level (Low/Medium/High)
Suggested safe routes and timings
Users must receive:
Real-time alerts when entering a high-risk zone
Warnings about hotspots along a selected route
2.2 Admin/Authority Module
Admin must be able to view:
Live hotspot dashboard
Filter by date/time/location
Clustered incidents and risk score distribution
Admin may mark verified incidents (optional)
2.3 ML Processing Module
System must aggregate all user-reported incidents.
ML module must process:
Clustering using K-Means (or DBSCAN optional)
Time-based risk segmentation
System must compute:
Risk scoring for each zone
Updating heatmap in real-time or fixed intervals
2.4 Map & Visualization Module
Must display:
Heatmaps
Markers for reports
Color-coded risk zones
Must integrate with:
Leaflet.js or Mapbox
Must allow:
Zoom, pan, and route selection
3. Non-Functional Requirements
3.1 Performance
Heatmap must load within 3–5 seconds.
Risk model should update within 1–2 seconds after new data is added.
3.2 Usability
Clean, minimal UI.
Single-click or tap to report incidents.
Accessible on mobile and desktop.
3.3 Scalability
Must support thousands of incident reports.
Must handle multiple cities in future versions.
3.4 Security
User identity must remain anonymous.
Data encrypted in cloud (Firebase security rules).
3.5 Reliability
System should have 99% uptime on deployment.
Must prevent spam reporting through basic validation.
4. Technical Requirements
4.1 Frontend
ReactJS / HTML / CSS / JavaScript
Leaflet.js or Mapbox for maps
Responsive UI
4.2 Backend
Firebase Firestore or Realtime Database
Optional: Node.js functions for processing
4.3 Machine Learning
Python (Pandas, Scikit-learn)
K-Means clustering
Time-of-day pattern analysis
Risk scoring algorithm
4.4 Deployment
Netlify / Vercel for frontend
Firebase Hosting/Cloud Functions
Free-tier friendly cloud setup
5. System Architecture Overview
Modules:
User Mobile/Web App
Report Collection API
ML Risk Analysis Engine
Firestore Database
Heatmap Visualization Layer
Admin Dashboard
Architecture ensures:
Real-time data flow
Secure and scalable cloud storage
ML-driven hotspot calculation
6. Data Requirements
User location coordinates
Timestamp of report
Type of incident
Clustered dataset for ML
Map tile data (OpenStreetMap / Mapbox)
7. Limitations
Accuracy depends on volume of reports
Requires stable internet connection
Cannot guarantee prevention, only prediction
8. Future Enhancements
NLP-based incident categorization
Predictive routing using LSTM
Integration with city transport APIs
Trusted reporter verification
Offline reporting option
