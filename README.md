🔗 URL Shortener System

📌 Project Overview

This project implements a URL Shortener system that converts long URLs into short, unique URLs and redirects users efficiently.
The system is designed keeping scalability, low latency, and collision-free URL generation in mind, similar to real-world systems like Bitly / TinyURL.

This project is part of System Design (SD) experimentation.

📂 Project Structure

EXPERIMENT_1/
│
├── app.py                     # Main application file
├── counterApproach.py         # Counter-based short URL generation
├── shortURLalreadyExist.py    # Handling duplicate URLs
├── URL_SHORTENER.drawio       # System design architecture diagram
├── URL_SHORTENER.jpg          # Architecture diagram image
├── 23BCS12433_SD_REPORT FILE.pdf  # Experiment report
└── README.md                  # Project documentation

⚙️ Functional Requirements

Convert long URLs into short URLs

Redirect short URLs to original URLs

Avoid duplicate short URL generation

Maintain mapping between short and long URLs

🚦 Non-Functional Requirements

Low latency redirection

High availability

Scalability for large number of URLs

Reliability (no broken links)

🧠 Implementation Details
🔹 app.py

Entry point of the application

Handles user input and URL redirection logic

Integrates different components of the system

🔹 counterApproach.py

Implements counter-based approach for short URL generation

Uses incremental counters to ensure uniqueness

Counter value is encoded to generate short URLs

🔹 shortURLalreadyExist.py

Checks if a URL already exists in the system

Prevents duplicate short URL creation

Ensures idempotent behavior

📐 System Design
High-Level Flow

User submits a long URL

System checks if URL already exists

If not:

Generate a unique ID using counter approach

Convert ID into short URL

Store mapping in storage

On accessing short URL:

Redirect user to original URL

🗄 Data Storage (Conceptual)

Short URL → Long URL mapping

Counter value for ID generation

🖼 Architecture Diagram

URL_SHORTENER.drawio – Editable system design diagram

URL_SHORTENER.jpg – Exported image for report & presentation

🧪 How to Run the Project

cd EXPERIMENT_1
python app.py

📊 Key System Design Concepts Used

Unique ID generation

Read-heavy optimization

Collision handling

Separation of concerns

Scalable design principles

🚀 Future Enhancements

Database integration (MySQL / MongoDB)

Redis caching

REST APIs

Analytics (click count)

User authentication

Expiry-based URLs

👨‍💻 Author
# 23BCS12433_PANKAJ_KUMAR_KRG3B
System Design – URL Shortener Project

📘 Academic Note

This project is developed as part of System Design coursework to understand real-world scalable system architectures.



































































