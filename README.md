# Smart Bus Monitoring System

## Overview
The **Smart Bus Monitoring System** is an AI-driven solution designed to revolutionize urban public transportation by optimizing bus scheduling, route planning, and passenger experience. It leverages real-time data, machine learning, and advanced technologies like GPS, GIS, and OCR to enhance efficiency, reduce delays, and streamline operations for both passengers and transport authorities.

This project was developed as part of a study at **IFET College of Engineering** under the **Department of Artificial Intelligence and Machine Learning**.

## Features
- **Real-Time Bus Tracking**: Utilizes GPS and GIS for live tracking of buses, providing accurate location updates to passengers and administrators.
- **Dynamic Route Optimization**: Integrates Google Maps API (Directions and Distance Matrix APIs) to calculate optimal routes, avoiding congested roads and redundant paths.
- **Traffic Prediction**: Employs machine learning models (e.g., neural networks, regression) to forecast traffic conditions, enabling proactive route adjustments.
- **OCR-Based Attendance Tracking**: Automatically recognizes bus number plates using Optical Character Recognition (OCR) to log arrival/departure times, reducing manual errors.
- **Automated Scheduling**:
  - **Linked Scheduling**: Assigns specific crews to buses for an entire shift.
  - **Unlinked Scheduling**: Dynamically reassigns rested crews to different buses and routes based on calculated rest hours.
- **Responsive User Interface**: Built with Bootstrap for a seamless and user-friendly experience across devices.
- **Scalable Backend**: Uses Django and PostgreSQL to handle large datasets and ensure robust performance.

## Tech Stack
- **Frontend**: Bootstrap (responsive UI design)
- **Backend**: Django (web framework)
- **Database**: PostgreSQL (scalable data storage)
- **APIs**: Google Maps API (Directions API, Distance Matrix API)
- **Machine Learning**: Python-based ML models (neural networks, regression) for traffic prediction
- **OCR**: Optical Character Recognition for bus number plate recognition
- **Geospatial Tools**: GPS and GIS for real-time tracking and route planning
- **Other**: Flask (optional for lightweight API endpoints), Transport datasets

## Project Structure
```
smart-bus-monitoring/
├── static/
│   ├── css/                  # Bootstrap and custom styles
│   ├── js/                   # Frontend scripts
│   └── images/               # Sample images (e.g., bus number plates)
├── templates/                # HTML templates for Django
├── datasets/                 # Transport and traffic datasets
├── ml_models/                # Machine learning models for traffic prediction
├── ocr/                      # OCR scripts for number plate recognition
├── routes/                   # Route optimization logic
├── scheduler/                # Bus and crew scheduling logic
├── manage.py                 # Django management script
├── README.md                 # Project documentation
└── requirements.txt          # Python dependencies
```

## Installation
### Prerequisites
- Python 3.8+
- PostgreSQL
- Google Maps API Key
- Node.js (for Bootstrap dependencies, if needed)
- pip (Python package manager)

### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/smart-bus-monitoring.git
   cd smart-bus-monitoring
   ```

2. **Set Up Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**:
   - Create a `.env` file in the root directory.
   - Add the following:
     ```
     GOOGLE_MAPS_API_KEY=your_api_key
     DATABASE_URL=postgresql://user:password@localhost:5432/smartbus
     ```

5. **Set Up PostgreSQL Database**:
   - Create a database named `smartbus`.
   - Run migrations:
     ```bash
     python manage.py migrate
     ```

6. **Run the Development Server**:
   ```bash
   python manage.py runserver
   ```

7. **Access the Application**:
   - Open a browser and navigate to `http://localhost:8000`.

## Usage
- **Admin Dashboard**: Log in to manage bus schedules, crew assignments, and view real-time tracking data.
- **Passenger Interface**: Check live bus locations, estimated arrival times, and optimal routes.
- **OCR Module**: Automatically logs bus attendance by processing number plate images.
- **Traffic Prediction**: View predicted traffic conditions and suggested route adjustments.

## Limitations
- **Incomplete Features**: Some modules (e.g., full OCR integration, advanced ML models) are partially implemented and require further development.
- **Integration Challenges**: Compatibility issues between technologies may arise during deployment.
- **Data Dependency**: Relies on accurate GPS signals and comprehensive transport datasets.
- **Performance**: Real-time processing may be resource-intensive for large fleets.

## Future Enhancements
- Fully implement OCR for real-time number plate recognition with higher accuracy.
- Enhance ML models with continuous learning for better traffic predictions.
- Add mobile app support for passengers and crew.
- Integrate IoT devices for additional real-time data (e.g., passenger count sensors).

## Feasibility & Viability
- **Technical Viability**: Robust tech stack ensures scalability and reliability.
- **Economic Benefits**: Reduces operational costs through automated scheduling and optimized routes.
- **Social Impact**: Improves passenger experience with accurate, real-time information.
- **Challenges**: Address integration issues and GPS inaccuracies through rigorous testing and error handling.

## References
1. *Smart Bus Real-Time Tracking System Using GSM and GPS Module* - SpringerLink
2. *The Algorithms Behind The Working Of Google Maps* - CodeChef
3. *Route Optimization & Real-Time Traffic* - Google Maps Platform
4. *A Survey of Optical Character Recognition Techniques* - N. S. Rathi, A. N. Sarode, R. Ghosh
5. *A Traffic Prediction Using Machine Learning: Literature Survey* - Ji Yoon Kim

## Acknowledgments
- **IFET College of Engineering** for providing the platform and resources.
- **Department of Artificial Intelligence and Machine Learning** for guidance.
- Presented by **Hariharan C**.

---

**Note**: This project is a work in progress. Contributions to complete the feature codebase are welcome!