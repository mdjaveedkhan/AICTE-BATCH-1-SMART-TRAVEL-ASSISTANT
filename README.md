# ✈️ AI Smart Travel Planner ASSISTANT

**Personalized AI-powered travel and itinerary planning — Generate seamless itineraries, transit logs, safety advisory briefs, and track budgets all in one place.**


---

## 🗺️ Problem & Solution

Traditional travel planning apps rely on static templates and generic routes that ignore what truly matters:

* Individual origins and varied home departure transits
* Real-time regional variables, documentation, and weather realities
* Strict budget tiers and destination-specific hidden costs
* Personal interests, hobbies, and traveler configurations
* Spontaneous planning adjustments on the go

This AI-powered travel agent uses **Google Gemini API** to tailor multi-variable schedules, destination strategies, and budget charts to match each user's exact requirements, ensuring every journey is practical, personalized, and fully exportable.

---

## 🛠️ Features

| Feature | Description |
| :--- | :--- |
| **Itinerary Generation** | Chronological day-by-day itineraries based on starting origin, destination, and interests. |
| **Logistics Advisory** | Custom transit routes via regional lines and neighborhood lodging choices filtered by budget tier. |
| **Local Guide Builder** | Structural advice covering regional weather adaptations, power socket standards, and survival phrases. |
| **Budget Mapping** | Dynamic calculation of daily spending variables processed into clean Markdown structures. |
| **Contextual Suggestions** | Built-in interactive recommended query buttons to fast-track testing loops without text fatigue. |
| **1-Click Portability** | Compiles structured itineraries into pure text files instant export via local file download modules. |

---

## 💻 Tech Stack

| Component | Technology |
| :--- | :--- |
| **Frontend** | Streamlit |
| **AI LLM Engine** | Google Gemini API (`models/gemini-2.5-flash`) |
| **Storage** | Session-State Persistent Data (`st.session_state`) with TXT Export |
| **Environment Control**| Python-dotenv (`.env` file isolation) |

---

## 📁 Project Structure

```text
├── app.py              # Main Streamlit web application orchestrator
├── requirements.txt       # Project dependencies and system requirements
└── README.md              # Project documentation report index
```

---

## 🚀 Installation

### Requirements
* Python 3.12
* pip package manager

### Setup

**1. Clone the repository**
```bash
git clone https://github.com
cd ai-travel-planner-agent
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Configure API Keys**
Create a `.env` file in the project root directory:

```env
GOOGLE_API_KEY=your_actual_gemini_api_key_here
```

> ⚠️ **Security Warning:** Never commit your `.env` file to public GitHub repositories. Ensure it is listed inside your `.gitignore` configuration.

### Obtain keys from:
* [Google AI Studio](https://google.com) — (Gemini API access dashboard)

---

## 🕹️ Usage

To launch your AI Travel Planner instance locally, execute:
```bash
streamlit run app.py
```
The web portal will automatically initialize inside your default browser window at `http://localhost:8501`.

---

## 🔧 Troubleshooting

| Issue | Solution |
| :--- | :--- |
| **API error: 429** | Gemini free-tier rate limit triggered. The application's automated exponential backoff loop will self-retry after 5 seconds. |
| **API error: 404** | API Version mismatched context. The script is pre-configured to override legacy routes via `http_options={"api_version": "v1"}`. |
| **Application Crash / Missing Data** | The download system utilizes state persistence loops. Keep download modules nested strictly inside conditional rendering paths to block data leaks. |
| **ImportErrors on launch** | Execute `pip install --upgrade google-genai streamlit python-dotenv pillow` to reset broken environment packages. |

---

## 👨‍💻 Author

**MD JAVEED KHAN**

Computer Science and Engineering Student  
Machine Learning & AI Enthusiast

Portfolio  
https://mdjaveedkhan.me

LinkedIn  
https://linkedin.com/in/mdjaveedkhan

Email  
mdjaveed1802@gmail.com

© 2026 Md Javeed Khan
