# FRAS (Facial Recognition Attendance System) – Internship Report
# Paste this file as, e.g., internship_report.yml in your GitHub repo.

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
  Replete Infotech Pvt Ltd is a leading IT company that provides technical solutions and services which strive to provide innovative and client-focused solutions, helping the customers modernise their networks inorder to providing excellence while ensuring quality customer service with our expert team, advanced technologies, and seamless processes. Replete Infotech Pvt Ltd strive to solve digital problems around us. From technology consulting to IT Services, they deliver the most innovative solutions with exceptional business value.
  Replete Infotech Pvt Ltd is one of the premium companies of India offering quality IT and ITES solutions to meet the new business challenges of the extremely competitive market. Their forte lies in product development and they have proved the same by successfully developing innovative products from time to time. They boast of a strong team of professionals who are certified developers with excellence in various IT fields to offer a bouquet of valuable services under a single roof. They are extremely committed to offer quality driven services and products to our worldwide clientele.

chapters:
  - chapter: 1
    title: "INTRODUCTION TO PROJECT"
    sections:
      - number: "1.1"
        title: "OBJECTIVE"
        content: |
          The objective of this project is to develop a comprehensive process of a facial recognition system using Python, showcasing the various stages involved from face detection to face recognition. This report aims to provide an in-depth understanding of the key packages and tools available in Python for facial recognition, the methods to improve accuracy, and the industry-standard practices employed. By detailing the implementation and evaluation of a facial recognition system, this report seeks to demonstrate the practical applications and potential improvements in this transformative technology across different industries.
      - number: "1.2"
        title: "DEFINITION"
        content: |
          Facial recognition is a sophisticated biometric technology that identifies or verifies individuals by analysing and comparing unique patterns based on their facial features. This technology utilizes advanced computer vision and machine learning algorithms to detect, align, encode, and match faces in images or video streams. The facial recognition process involves several critical steps: face detection to identify areas with faces, face alignment to standardize the orientation, face encoding to convert facial features into numerical codes, and face matching to compare these codes and determine identity.
          In the context of this report, facial recognition is implemented using Python's extensive ecosystem of libraries, including OpenCV, which offers versatile face detection algorithms, Dlib, known for its efficient face detection and shape prediction, and Face_recognition, which simplifies face recognition tasks. Facial recognition technology is widely applied in various fields, providing accurate and reliable identification solutions for security, surveillance, and human-computer interaction, thereby enhancing safety and user experience.

  - chapter: 2
    title: "PROJECT DESCRIPTION"
    content: |
      This project focuses on developing a robust and accurate facial recognition system using Python, leveraging its comprehensive ecosystem of libraries and tools. Facial recognition has revolutionized numerous industries, including security, surveillance, and human computer interaction, by providing reliable and efficient identification solutions. The project aims to explore and implement the various stages involved in facial recognition, from face detection to face recognition, using well-known Python libraries such as OpenCV, Dlib, and Face_recognition.
      The project is divided into several key components, each addressing a specific aspect of the facial recognition process.

    frontend_features:
      - "Sign-Up Page: Employees register with name, employee ID, mobile number, and email."
      - "Photo Upload: Employees upload photos required for recognition."
      - "Email Verification: OTP is sent via SMTP; user verifies email."
      - "Face Matching: Webcam capture compared to stored images."
      - "Punch In/Out and Break In/Out: Mark attendance and breaks."
      - "Geo-Tagging: Validates employee location during attendance."

    frontend_stack:
      - "HTML/CSS"
      - "JavaScript"
      - "Flask (templating + routes)"

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
        Photos are stored as LONG_BLOB. Indexes on employee_id and email improve lookup performance.

    backend_features:
      - "Image Capture & Processing with OpenCV."
      - "Face Matching using Face_recognition (Dlib) encodings."
      - "Similarity thresholds with Euclidean/Cosine metrics."
      - "SMTP integration for OTP email verification."
      - "Secure routes for attendance events and logs."

    recognition_pipeline:
      steps:
        - "Face Detection (Haar Cascades/Dlib HOG/CNN)."
        - "Face Alignment (landmarks-based)."
        - "Face Encoding (128-d embeddings)."
        - "Face Matching (Euclidean distance + threshold)."
      threshold_tuning: |
        The decision threshold balances false positives and false negatives. Multiple samples per user and lighting normalization improve robustness.

project_overview: |
  The Facial Recognition Attendance System (FRAS) is an AI-powered attendance solution built with Python, Flask, MySQL, OpenCV, Dlib, and Face_recognition. It automates employee attendance with OTP-verified signup, webcam-based recognition, geotag validation, and reliable punch/break logging.

internship_journey:
  weeks:
    - week: 1
      theme: "Setup & Understanding Basics"
      days:
        day1: "Introduction to internship & company profile (Replete Infotech Pvt Ltd)."
        day2: "Finalized project title and requirements."
        day3: "Explored Python libraries for face recognition (OpenCV, Dlib, Face_recognition)."
        day4: "Studied Flask framework basics."
        day5: "Installed dependencies and set up local environment."
        day6: "Designed high-level architecture of FRAS system."
        day7: "Prepared weekly documentation and synced with mentor."

    - week: 2
      theme: "Frontend & User Registration Module"
      days:
        day1: "Created basic frontend pages with HTML/CSS/JS."
        day2: "Developed Signup page with employee details form."
        day3: "Integrated photo upload feature."
        day4: "Implemented email OTP verification using SMTP."
        day5: "Tested validation for email & form submissions."
        day6: "Connected frontend forms with Flask backend APIs."
        day7: "Weekly review & commit to GitHub."

    - week: 3
      theme: "Database & Backend Core Setup"
      days:
        day1: "Designed MySQL schema for employee data, photos, and attendance logs."
        day2: "Implemented user registration & OTP storage in database."
        day3: "Created Flask routes for signup/login."
        day4: "Tested CRUD operations with MySQL."
        day5: "Optimized photo storage in LONG_BLOB format."
        day6: "Worked on Punch In/Out backend logic."
        day7: "Documentation & team sync."

    - week: 4
      theme: "Face Recognition Engine"
      days:
        day1: "Integrated webcam image capture with OpenCV."
        day2: "Applied face detection using Haar Cascades & Dlib."
        day3: "Implemented facial encoding with Face_recognition library."
        day4: "Face matching using Euclidean distance threshold."
        day5: "Optimized accuracy with multiple images per user & lighting tests."
        day6: "Tested live recognition with database images."
        day7: "Weekly review & bug fixing."

    - week: 5
      theme: "Attendance System Features"
      days:
        day1: "Implemented Punch In/Out and Break In/Out tracking."
        day2: "Added Geo-tagging support for location validation."
        day3: "Developed dashboard views for attendance logs."
        day4: "UI improvements for employee interaction."
        day5: "Backend validations for duplicate entries & time rules."
        day6: "Conducted system testing with sample users."
        day7: "Weekly summary & mentor review."

    - week: 6
      theme: "Finalization & Deployment"
      days:
        day1: "Fixed bugs & improved UI responsiveness."
        day2: "Security enhancements (password hashing, input validation)."
        day3: "Prepared deployment setup (Flask + MySQL)."
        day4: "Finalized project report & documentation."
        day5: "Conducted final testing with mentors."
        day6: "Submitted final project & presentation."
        day7: "Internship wrap-up & feedback session."

key_features:
  - "Employee Registration with Photo Upload"
  - "Email OTP Verification (SMTP)"
  - "Real-time Face Recognition via Webcam"
  - "Attendance Logging (Punch In/Out, Break In/Out)"
  - "Geo-tagging for Location Validation"
  - "MySQL Database with Secure Data Storage"
  - "Flask-based Backend with HTML/CSS/JS Frontend"

tech_stack:
  frontend: ["HTML", "CSS", "JavaScript"]
  backend: ["Python", "Flask"]
  database: ["MySQL"]
  libraries: ["OpenCV", "Dlib", "Face_recognition", "NumPy"]
  authentication: ["Email OTP (SMTP)"]
  deployment: ["Localhost", "Optional: Cloud/VM"]

results:
  - "Functional facial recognition attendance system built and tested."
  - "High recognition accuracy achieved with multiple samples per user."
  - "Secure OTP verification and geolocation validation implemented."
  - "Automated logging reduces manual errors and proxy attendance."

future_work:
  - "Multi-factor authentication (biometrics + OTP)."
  - "Cloud storage & CDN for image management."
  - "Admin dashboard with analytics and exportable reports."
  - "Mobile app integration for remote check-ins."
  - "Emotion/mood detection module (responsible AI considerations)."

acknowledgments: |
  I sincerely thank Replete Infotech Pvt Ltd, my mentors, faculty members, and peers for their guidance and support during this internship. Special thanks to the open-source community for Python, OpenCV, Flask, and MySQL for providing powerful tools that made this project possible.

references:
  - "OpenCV Documentation"
  - "Flask Documentation"
  - "MySQL Official Docs"
  - "Dlib & Face_recognition Libraries"
  - "Python smtplib Documentation"

author:
  name: "Jay Bhatt"
  portfolio: "https://jaybhatt375453.github.io"
  linkedin: "https://www.linkedin.com/in/jaybhatt375453/"
  github: "https://github.com/jaybhatt375453"

sample_code:
  flask_otp_route: |
    # Example: Flask route to send OTP via SMTP (simplified)
    import os
    import smtplib
    import random
    from email.mime.text import MIMEText
    from flask import Flask, request, jsonify
    import mysql.connector
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

      return jsonify({"message":"OTP sent"})

  recognition_snippet: |
    # Example: Face encoding & matching with face_recognition
    import cv2
    import face_recognition
    import numpy as np

    # Load known images (from DB or filesystem)
    known_images = [
      ("EMP001", face_recognition.load_image_file("samples/emp001_1.jpg")),
      ("EMP002", face_recognition.load_image_file("samples/emp002_1.jpg")),
    ]
    known_encodings = []
    known_labels = []
    for label, img in known_images:
      encs = face_recognition.face_encodings(img)
      if encs:
        known_encodings.append(encs[0])
        known_labels.append(label)

    # Capture frame from webcam
    cap = cv2.VideoCapture(0)
    ret, frame = cap.read()
    cap.release()

    rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    boxes = face_recognition.face_locations(rgb, model="hog")  # or "cnn"
    encodings = face_recognition.face_encodings(rgb, boxes)

    match_label = None
    threshold = 0.5  # tune this value based on validation

    for enc in encodings:
      distances = face_recognition.face_distance(known_encodings, enc)
      idx = np.argmin(distances) if len(distances) else None
      if idx is not None and distances[idx] <= threshold:
        match_label = known_labels[idx]
        break

    print("Match:", match_label if match_label else "No match")
