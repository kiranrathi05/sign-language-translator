# 🤟 SignSpire: Indian Sign Language Animation Generator

SignSpire is an assistive web application that converts plaintext sentences into dynamic Indian Sign Language (ISL) animations using a stick-figure avatar. The project aims to make digital content more accessible to Deaf and Hard-of-Hearing users across India by bridging the communication gap through technology.

---
## 🚀 Features

- ✍️ Text-to-ISL Conversion
  Converts plaintext sentences into Indian Sign Language animations, represented by a stick-figure avatar.

- 📊 Indexed Sign Data
  Uses pre-indexed ISL data stored in JSON files (pose_files_urls_A.json to pose_files_urls_Z.json) for efficient mapping of words to signs.

- 🎥 Dynamic Animation Generation
  Generates smooth ISL animations using generate_dynamic_video.py, ensuring natural and accurate sign representation.

- 🛠️ Data Preprocessing
  Includes scripts for correcting and smoothing pose data (correcting_pose.py, smoothing.py) to enhance animation quality.

- 🔎 Lookup Functionality
  Provides efficient lookup of ISL signs through lookup.py for real-time animation generation.

- 💻 React-Based Frontend
  A modern web interface built with React (App.jsx, main.jsx) for users to input text and view ISL animations.

- 🔧 Configuration Management
  Uses Vite for frontend development (vite.config.js) and manages dependencies with package.json.

---

## 📁 Project Structure
```

SignSpire/
├── SIGNBackend/                       # Backend logic for ISL processing
│   ├── INDEXES/                       # Directory for indexed ISL data
│   │   ├── pose_files_urls_A.json     # ISL pose data for category A
│   │   ├── pose_files_urls_B.json     # ISL pose data for category B
│   │   ├── pose_files_urls_C.json     # ISL pose data for category C
│   │   ├── pose_files_urls_D.json     # ISL pose data for category D
│   │   ├── pose_files_urls_E.json     # ISL pose data for category E
│   │   ├── pose_files_urls_F.json     # ISL pose data for category F
│   │   ├── pose_files_urls_G.json     # ISL pose data for category G
│   │   ├── pose_files_urls_H.json     # ISL pose data for category H
│   │   ├── pose_files_urls_I.json     # ISL pose data for category I
│   │   ├── pose_files_urls_J.json     # ISL pose data for category J
│   │   ├── pose_files_urls_K.json     # ISL pose data for category K
│   │   ├── pose_files_urls_L.json     # ISL pose data for category L
│   │   ├── pose_files_urls_M.json     # ISL pose data for category M
│   │   ├── pose_files_urls_N.json     # ISL pose data for category N
│   │   ├── pose_files_urls_O.json     # ISL pose data for category O
│   │   ├── pose_files_urls_P.json     # ISL pose data for category P
│   │   ├── pose_files_urls_Q.json     # ISL pose data for category Q
│   │   ├── pose_files_urls_R.json     # ISL pose data for category R
│   │   ├── pose_files_urls_S.json     # ISL pose data for category S
│   │   ├── pose_files_urls_T.json     # ISL pose data for category T
│   │   ├── pose_files_urls_U.json     # ISL pose data for category U
│   │   ├── pose_files_urls_V.json     # ISL pose data for category V
│   │   ├── pose_files_urls_W.json     # ISL pose data for category W
│   │   ├── pose_files_urls_Y.json     # ISL pose data for category Y
│   │   └── pose_files_urls_Z.json     # ISL pose data for category Z
│   ├── concatenate.py                 # Script for concatenating ISL data
│   ├── correcting_pose.py             # Script for correcting pose data
│   ├── generate_dynamic_video.py      # Script for generating ISL animations
│   ├── lookup.py                      # Script for looking up ISL signs
│   ├── main.py                        # Entry point for the backend
│   ├── requirements.txt               # Python dependencies list
│   └── smoothing.py                   # Script for smoothing pose data
│
├── SIGNFrontend/                      # Frontend for user interaction
│   ├── public/                        # Public assets
│   │   └── vite.svg                   # Vite logo (optional)
│   ├── src/                           # Source files for React frontend
│   │   ├── assets/                    # Static assets like images
│   │   │   └── react.svg              # React logo (optional)
│   │   ├── App.css                    # Styles for the main app component
│   │   ├── App.jsx                    # Main React component
│   │   ├── index.css                  # Global styles
│   │   └── main.jsx                   # Entry point for React app
│   ├── .gitignore                     # Git ignore file
│   ├── README.md                      # Frontend-specific README
│   ├── eslint.config.js               # ESLint configuration
│   ├── index.html                     # Main HTML file for the frontend
│   ├── package-lock.json              # NPM dependency lock file
│   ├── package.json                   # NPM dependencies and scripts
│   └── vite.config.js                 # Vite configuration for frontend build
│
├── .gitignore                         # Git ignore file for the project
└── README.md                          # Project documentation (this file)

```
---

<details>

## 🔧 Installation

1. Clone the repository

  - git clone <repository-url>
  
  - cd SignSpire

2. Set up the backend

    - Create a virtual environment
     
       - **python** -m venv venv

       - **source** venv/bin/activate  # or `venv\Scripts\activate` on Windows

   - Install Python dependencies:

       - cd SIGNBackend
     
       - pip install -r requirements.txt

3. Set up the frontend

  - Navigate to the frontend directory:
    - cd SIGNFrontend

  - Install Node.js dependencies:
    - npm install

4. Run the application

  - Start the backend:
     - cd SIGNBackend
     - python main.py

  - Start the frontend:
     - cd SIGNFrontend
     - npm run dev

  - Open your browser and navigate to http://localhost:5173 (or the port specified by Vite) to access the SignSpire interface.

---

## 🧠 How It Works

- The backend (SIGNBackend) processes plaintext input and maps words to ISL signs using indexed data in JSON files (pose_files_urls_A.json to pose_files_urls_Z.json).

- Scripts like correcting_pose.py and smoothing.py ensure the pose data is accurate and smooth for animation.

- The lookup.py script retrieves the corresponding ISL signs for each word in the input sentence.

- The generate_dynamic_video.py script creates a stick-figure animation of the ISL signs.

- The frontend (SIGNFrontend) provides a user interface built with React, allowing users to input text and view the resulting ISL animation.

---

## 💻 Usage Examples

-🎙️ Voice / Text Commands  

| 🧠 **Command Type** | 🎤 **Example Voice or Chat Command** | 💡 **What Happens** |
|--------------------|---------------------------------------|---------------------|
| **Text → ISL** | “Translate **Good morning, everyone** to ISL.” | Generates a stick-figure animation for the full sentence. |
| **Word Lookup** | “Show me the sign for **responsibility**.” | Returns pose data, gloss info, and a preview clip. |
| **Pose Smoothing** | “Smooth the pose data for **hello.json**.” | Runs the smoothing engine and gives back a refined JSON. |
| **Video Export** | “Create a **1080p** video for **thank you** with cinematic camera.” | Calls `generate_dynamic_video.py` and outputs an MP4. |
| **Database Stats** | “How many words are in the Signspire DB?” | Replies with the current gloss count (e.g., **1 100 words**). |
| **Version Check** | “What’s new in **Signspire 2.0**?” | Lists the latest features from the changelog. |

> **Tip:** Say “Help” (or type `help`) at any time to hear the full capability list.

---

## 💻 Developer Quick-Reference  

| **Action / Script**             | **Sample Command**                                     | **What It Does** |
|---------------------------------|--------------------------------------------------------|------------------|
| **Convert Text → ISL**          | *(web UI)*                                            | Renders a sentence-level ISL animation. |
| **Look up an ISL Sign**         | `python lookup.py "hello"`                            | Prints pose JSON + gloss metadata. |
| **Smooth Pose Data**            | `python smoothing.py poses.json`                      | Applies temporal/bézier smoothing. |
| **Generate Full Animation**     | `python generate_dynamic_video.py --input poses.json --out demo.mp4` | Creates an HD video with camera motion. |

---

## 🔄 Version Comparison  

| 🔢 **Version** | ✨ **Features Added** |
|---------------|-----------------------|
| **v1.0** | • Sentence-level text-to-ISL conversion<br>• Word lookup CLI |
| **v1.5** | • Pose-correction heuristics<br>• Smoothing script |
| **v2.0** | • React frontend with live preview<br>• Dynamic video generation |
| **v2.5&nbsp;(Upcoming)** | • Emotion/tone modifiers<br>• Web dashboard for batch jobs<br>• Multi-language captions |

---



## 🔮 Future Enhancements

| 🚀 **Planned Feature** | 📝 **Description** |
|------------------------|--------------------|
| **🗣️ Speech-to-ISL** | Integrate speech-recognition (Whisper / Vosk) to turn **spoken sentences** directly into animated ISL. |
| **🌍 Multi-Language Support** | Expand the engine and gloss DB to cover **ASL, BSL, and regional Indian dialects**, with automatic language detection. |
| **🎨 Custom Avatars** | Let users pick body type, skin tone, clothing, and animation style for a **personalized signing avatar**. |
| **📱 Mobile App** | Build **Android / iOS** apps with on-device inference for offline use and broader accessibility. |

---

## 🤝 Contribute

We ❤️ community ideas and pull requests!

1. **Fork** the repo and create a feature branch.  
2. **Code** your improvement and add tests / docs.  
3. **Open a PR** describing the change and link any related issues.  
4. Join the discussion—feedback is welcomed and iterative.

I welcome contributions and ideas. If you have blog suggestions or freelance opportunities, feel free to contact me via DM on socials.

*Let’s make sign language technology accessible to everyone!* ✋✨


</details>
