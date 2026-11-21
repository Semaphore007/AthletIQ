# 🏋️ AthletIQ – AI-Powered Real-Time Fitness Coach

**Your Personal AI Fitness Trainer | Real-Time Pose Detection | Intelligent Workout Tracking | AI Voice Coaching**

AthletIQ is an AI-powered fitness coaching application that leverages computer vision, pose estimation, and Large Language Models (LLMs) to provide real-time workout monitoring and intelligent exercise guidance. It analyzes body movements through a webcam, tracks exercise repetitions, evaluates workout form, and delivers personalized coaching feedback through voice assistance.

The platform aims to make intelligent fitness coaching more accessible by combining computer vision and generative AI into an interactive workout experience.

---

## ✨ Key Features

- **Real-Time Pose Detection:** Tracks body movements and landmarks using MediaPipe.
- **Automatic Rep Counting:** Detects exercise movements and automatically counts repetitions.
- **Exercise Recognition:** Supports multiple workout activities through dedicated exercise detectors.
- **Form Analysis:** Evaluates body positioning, joint angles, and movement patterns.
- **AI-Powered Coaching:** Integrates Large Language Models to generate intelligent workout feedback.
- **Voice-Based Assistance:** Converts coaching feedback into speech for an interactive training experience.
- **Workout Tracking:** Monitors exercise performance, repetitions, and workout progress.
- **Workout History:** Maintains user workout records using SQLite.
- **Interactive Dashboard:** Provides a Streamlit-based interface for workout monitoring.
- **Dedicated Landing Page:** Includes a separate website introducing the fitness coaching platform.

## 🏋️ Supported Exercises

| Exercise | Functionality |
|---|---|
| Squats | Movement analysis and repetition counting |
| Push-ups | Body movement and exercise tracking |
| Biceps Curls | Arm movement analysis |
| Shoulder Press | Upper-body movement tracking |
| Lunges | Lower-body movement analysis |

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend / UI | Streamlit, HTML, CSS, JavaScript |
| Computer Vision | OpenCV |
| Pose Estimation | MediaPipe |
| Video Streaming | Streamlit WebRTC |
| Generative AI | Groq API, LLM Integration |
| Voice Assistance | Google Text-to-Speech (gTTS) |
| Database | SQLite |
| Data Processing | NumPy, Pandas |
| Configuration | Python-dotenv |

## 🧠 System Architecture

AthletIQ follows a modular architecture combining computer vision, exercise detection, AI-based coaching, and workout persistence.

```text
             User / Webcam
                   |
                   v
          Real-Time Video Stream
                   |
                   v
           Video Processing
                   |
                   v
         MediaPipe Pose Detection
                   |
                   v
          Body Landmark Extraction
                   |
                   v
         Exercise-Specific Detectors
                   |
                   v
        Movement & Form Analysis
                   |
          +--------+--------+
          |                 |
          v                 v
     Rep Counting      Form Evaluation
          |                 |
          +--------+--------+
                   |
                   v
           Workout Metrics
                   |
          +--------+--------+
          |                 |
          v                 v
      LLM Coaching      SQLite Storage
          |
          v
      Text-to-Speech
          |
          v
    Real-Time Voice Feedback
```

## 📂 Project Structure

```text
AthletIQ/
│
├── LandingPage/
│   ├── IMGs/
│   ├── fonts/
│   ├── index.html
│   └── style.css
│
├── Main App/
│   │
│   ├── core/
│   │   └── base_exercise.py
│   │
│   ├── detectors/
│   │   ├── squat.py
│   │   ├── pushup.py
│   │   ├── biceps_curl.py
│   │   ├── shoulder_press.py
│   │   └── lunges.py
│   │
│   ├── ml_models/
│   │
│   ├── pages/
│   │
│   ├── services/
│   │   ├── auth/
│   │   ├── coaching/
│   │   ├── config/
│   │   ├── persistence/
│   │   ├── state/
│   │   ├── tracking/
│   │   ├── ui/
│   │   └── vision/
│   │
│   ├── static/
│   ├── tutorial-info/
│   ├── main.py
│   ├── requirements.txt
│   └── packages.txt
│
├── .gitignore
└── README.md
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/shradha-khapra/ai-gym-coach.git
```

### 2. Navigate to the Project

```bash
cd ai-gym-coach
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 4. Install Dependencies

Navigate to the main application directory:

```bash
cd "Main App"
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### 5. Configure API Credentials

Configure your Groq API key for LLM-powered coaching.

Create a `.env` file in the appropriate application directory:

```env
GROQ_API_KEY=your_groq_api_key
```

Obtain your API credentials from the Groq developer platform.

**Important:** Never commit API keys or other sensitive credentials to GitHub.

## ▶️ Running the Application

From the `Main App` directory, execute:

```bash
streamlit run main.py
```

The application will be available at:

```text
http://localhost:8501
```

Open the URL in your browser and allow camera access when prompted.

## 🌐 Running the Landing Page

Open another terminal from the project root:

```bash
cd LandingPage
```

Start a local development server:

```bash
python -m http.server 5500
```

Access the landing page:

```text
http://localhost:5500
```

## 🔍 How It Works

1. **Video Acquisition:** Captures live video through the user's webcam.
2. **Pose Estimation:** MediaPipe identifies body landmarks and tracks movement.
3. **Exercise Detection:** Dedicated detection modules process exercise-specific movements.
4. **Movement Analysis:** Evaluates joint positions and movement patterns.
5. **Repetition Tracking:** Identifies exercise repetitions and updates workout metrics.
6. **AI Coaching:** Uses LLM integration to generate contextual workout feedback.
7. **Voice Feedback:** Converts generated coaching responses into speech.
8. **Workout Persistence:** Stores relevant workout records for future reference.

## 🔮 Future Enhancements

- Personalized workout recommendations.
- Advanced exercise form scoring.
- Fatigue and movement consistency analysis.
- Progress visualization and analytics.
- Additional exercise recognition models.
- Mobile-friendly fitness coaching experience.

## 🎯 Project Objectives

- Apply computer vision to real-world fitness applications.
- Implement pose estimation for human movement analysis.
- Develop modular exercise detection and repetition tracking.
- Integrate LLMs for intelligent and contextual coaching.
- Build an interactive fitness platform with real-time voice assistance.
- Combine AI, software engineering, and data persistence into a practical application.

---

## 👨‍💻 Project Information

**Project:** AthletIQ – AI-Powered Real-Time Fitness Coach

**Domain:** Artificial Intelligence | Machine Learning | Computer Vision | Generative AI

**Repository:** [GitHub – AI Gym Coach](https://github.com/shradha-khapra/ai-gym-coach)

**Built with:** Python, MediaPipe, OpenCV, Streamlit, Groq API, and SQLite.

---

⭐ If you find this project interesting, consider starring the repository!
