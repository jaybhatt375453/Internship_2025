# ==============================================
#  FRAS (Facial Recognition Attendance System)
#  Internship Report - Summer Internship 2025
#  Author: Jay Bhatt (22IT008 | CSPIT-IT)
# ==============================================

meta:
  title: "Facial Recognition Attendance System (FRAS)"
  type: "Internship Report"
  duration: "6 Weeks (Summer Internship 2025)"
  intern:
    name: "Jay Bhatt"
    student_id: "22IT008"
    institute: "CSPIT-IT"
  mentor: "[Mentor Name / Replete Infotech Pvt Ltd]"
  repository: "https://github.com/<your-username>/<your-repo>"
  live_demo: "https://<your-deployment-link>"
  company: "Replete Infotech Pvt Ltd"

company_description: |
  Replete Infotech Pvt Ltd is a leading IT company providing innovative digital solutions, modernizing business networks, and delivering exceptional client-centric IT services. 
  With expertise in **technology consulting, IT services, and product development**, the company specializes in building robust software solutions using modern technologies. 
  Their strength lies in a highly skilled team of certified developers, who deliver quality-driven solutions across domains such as **cloud computing, artificial intelligence, data analytics, and web technologies**. 
  Replete Infotech Pvt Ltd has established itself as a trusted partner for businesses aiming to thrive in today’s competitive digital landscape.

chapters:
  - chapter: 1
    title: "INTRODUCTION TO PROJECT"
    sections:
      - number: "1.1"
        title: "Objective"
        content: |
          The objective of this project is to design and implement a **Facial Recognition Attendance System (FRAS)** using Python and modern libraries. 
          The system automates employee attendance tracking with face recognition, OTP-based verification, and geolocation validation. 
          This project aims to highlight the potential of AI-powered attendance systems in **reducing proxy attendance, improving accuracy, and enhancing workplace security.**
      - number: "1.2"
        title: "Definition"
        content: |
          Facial recognition is a **biometric identification technique** that verifies individuals by analyzing unique facial patterns. 
          It uses advanced algorithms for:
            - **Face Detection** (locating faces in images/video),
            - **Face Alignment** (normalizing positions),
            - **Face Encoding** (numerical representation of features),
            - **Face Matching** (comparison with stored encodings).
          In this project, Python libraries such as **OpenCV, Dlib, and Face_recognition** are used to achieve high-accuracy recognition.
          Applications extend to **security, surveillance, authentication systems, and time/attendance automation.**

  - chapter: 2
    title: "PROJECT DESCRIPTION"
    content: |
      The **FRAS Project** is divided into modular components for frontend, backend, and recognition logic. 
      It is built using **Python, Flask, MySQL, and AI-based recognition libraries.** 
      The system ensures secure attendance tracking with features like OTP authentication, webcam-based recognition, punch/break logs, and geotagging.

    frontend_features:
      - "Sign-Up Page: Employee registration with details and photo upload."
      - "Email OTP Verification: Secure email validation via SMTP."
      - "Face Matching: Real-time webcam-based recognition."
      - "Punch In/Out & Break In/Out: Attendance and work-break tracking."
      - "Geo-Tagging: Ensures employee is at designated location."

    frontend_stack:
      - "HTML5 / CSS3"
      - "JavaScript (Validation, UI Interaction)"
      - "Flask (Templating & Routing)"

    database_design:
      engine: "MySQL"
      entities:
        - name: "employees"
          fields: ["id", "name", "employee_id", "mobile", "email", "photo_longblob", "created_at"]
        - name: "attendance_logs"
          fields: ["id", "employee_id", "type (punch_in|punch_out|break_in|break_out)", "timestamp", "geotag_lat", "geotag_lng"]
        - name: "otps"
          fields: ["id", "email", "otp_code", "expires_at", "consumed (bool)"]
      notes: |
        - Photos stored as **LONG_BLOB**.  
        - Indexes on `employee_id` and `email` improve search performance.  
        - Attendance logs linked with employee IDs for traceability.  

    backend_features:
      - "Image Capture & Preprocessing with OpenCV."
      - "Face Recognition using Dlib & Face_recognition encodings."
      - "Distance-based face matching (Euclidean threshold)."
      - "SMTP-based OTP authentication."
      - "Flask REST routes for attendance events."

    recognition_pipeline:
      steps:
        - "Face Detection → Haar Cascades / Dlib HOG"
        - "Face Alignment → Landmark correction"
        - "Face Encoding → 128-d embeddings"
        - "Face Matching → Euclidean distance threshold"
      threshold_tuning: |
        Thresholds are tuned to **minimize false positives/negatives**. 
        Techniques such as **multiple sample images, lighting normalization, and angle adjustments** were applied to boost accuracy.

project_overview: |
  FRAS provides an **AI-powered attendance solution** that integrates:
    - OTP-verified signup,
    - Real-time face recognition,
    - Secure database logging,
    - Location-based validation.  
  Built with **Flask, Python, MySQL, OpenCV, and Face_recognition**, it ensures an accurate and reliable replacement for traditional attendance systems.

internship_journey:
  weeks:
    - week: 1
      theme: "Setup & Basics"
      highlights:
        - Company induction & project briefing
        - Environment setup (Python, Flask, MySQL, OpenCV)
        - Research on facial recognition techniques
    - week: 2
      theme: "Frontend Development"
      highlights:
        - Built Signup & Login pages
        - Integrated email OTP validation
        - Linked frontend with Flask routes
    - week: 3
      theme: "Database & API Integration"
      highlights:
        - Designed MySQL schema for employees, OTPs, and logs
        - Integrated database CRUD with Flask
        - Developed attendance APIs
    - week: 4
      theme: "Face Recognition Module"
      highlights:
        - Implemented detection & encoding
        - Optimized recognition pipeline
        - Tested accuracy with multiple users
    - week: 5
      theme: "Attendance Features"
      highlights:
        - Added Punch & Break In/Out
        - Integrated Geo-tagging validation
        - Created dashboard for logs
    - week: 6
      theme: "Finalization & Deployment"
      highlights:
        - Bug fixes & UI improvements
        - Deployment-ready build
        - Final presentation & documentation

key_features:
  - "Employee Registration with Photo Upload"
  - "Secure OTP-based Email Verification"
  - "Webcam-based Real-time Face Recognition"
  - "Punch In/Out & Break In/Out Tracking"
  - "Geo-tagging for Location Validation"
  - "MySQL Database for Logs & User Data"
  - "Flask-based RESTful Backend"

tech_stack:
  frontend: ["HTML5", "CSS3", "JavaScript"]
  backend: ["Python", "Flask"]
  database: ["MySQL"]
  libraries: ["OpenCV", "Dlib", "Face_recognition", "NumPy"]
  authentication: ["SMTP (Email OTP)"]
  deployment: ["Localhost", "Cloud-ready (VM/Heroku/Docker)"]

results:
  - "Successfully built a functional attendance system."
  - "Achieved >90% recognition accuracy with optimized threshold."
  - "Reduced risk of proxy attendance with AI-driven validation."
  - "Secured workflow with OTP & geo-validation."

future_work:
  - "Multi-factor authentication (Face + OTP + RFID)."
  - "Cloud-based image storage with CDN."
  - "Admin Dashboard with Analytics & Reports."
  - "Mobile App Integration for remote check-ins."
  - "AI-powered Emotion Detection (Ethical Considerations)."

acknowledgments: |
  I sincerely thank **Replete Infotech Pvt Ltd**, my mentors, and faculty at CSPIT-IT for their support and guidance.  
  Special gratitude to the **open-source community** of Python, Flask, OpenCV, Dlib, and Face_recognition for providing powerful libraries that made this project possible.

references:
  - "OpenCV Documentation"
  - "Flask Framework Docs"
  - "MySQL Official Documentation"
  - "Dlib & Face_recognition Library Guides"
  - "Python SMTP (smtplib) Docs"

author:
  name: "Jay Bhatt"
  portfolio: "https://jaybhatt375453.github.io"
  linkedin: "https://www.linkedin.com/in/jaybhatt375453/"
  github: "https://github.com/jaybhatt375453"

sample_code:
  flask_otp_route: |
    # Flask OTP Sending (SMTP + MySQL Integration)
    import os, smtplib, random, mysql.connector
    from flask import Flask, request, jsonify
    from email.mime.text import MIMEText
    from datetime import datetime, timedelta

    app = Flask(__name__)

    def db():
        return mysql.connector.connect(
            host=os.getenv("DB_HOST","localhost"),
            user=os.getenv("DB_USER","root"),
            password=os.getenv("DB_PASS",""),
            database=os.getenv("DB_NAME","fras")
        )

    @app.post("/auth/send-otp")
    def send_otp():
        email = request.json.get("email")
        if not email:
            return jsonify({"error":"email required"}), 400

        code = str(random.randint(100000, 999999))
        expires_at = (datetime.utcnow() + timedelta(minutes=10)).strftime("%Y-%m-%d %H:%M:%S")

        conn = db(); cur = conn.cursor()
        cur.execute("INSERT INTO otps (email, otp_code, expires_at, consumed) VALUES (%s,%s,%s,%s)",
                    (email, code, expires_at, False))
        conn.commit(); cur.close(); conn.close()

        msg = MIMEText(f"Your FRAS OTP is: {code}. It expires in 10 minutes.")
        msg["Subject"] = "FRAS Email Verification OTP"
        msg["From"] = os.getenv("SMTP_FROM")
        msg["To"] = email

        with smtplib.SMTP_SSL(os.getenv("SMTP_HOST","smtp.gmail.com"), int(os.getenv("SMTP_PORT","465"))) as s:
            s.login(os.getenv("SMTP_USER"), os.getenv("SMTP_PASS"))
            s.send_message(msg)

        return jsonify({"message":"OTP sent successfully!"})

  recognition_snippet: |
    # Face Recognition (OpenCV + Face_recognition)
    import cv2, face_recognition, numpy as np

    # Load known employee images
    known_images = [
        ("EMP001", face_recognition.load_image_file("samples/emp001.jpg")),
        ("EMP002", face_recognition.load_image_file("samples/emp002.jpg")),
    ]
    known_encodings, known_labels = [], []
    for label, img in known_images:
        encs = face_recognition.face_encodings(img)
        if encs:
            known_encodings.append(encs[0])
            known_labels.append(label)

    # Capture frame
    cap = cv2.VideoCapture(0)
    ret, frame = cap.read()
    cap.release()

    rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    boxes = face_recognition.face_locations(rgb, model="hog")
    encodings = face_recognition.face_encodings(rgb, boxes)

    match_label, threshold = None, 0.5
    for enc in encodings:
        distances = face_recognition.face_distance(known_encodings, enc)
        if len(distances):
            idx = np.argmin(distances)
            if distances[idx] <= threshold:
                match_label = known_labels[idx]
                break

    print("Recognition Result:", match_label if match_label else "No match found")
