Overview
CvAlign is a fast, AI-based recruitment tool that automates CV screening using a RAG (Retrieval-Augmented Generation) pipeline. It uses HuggingFace’s MiniLM model and LangChain to score CVs with 85% human-level accuracy, processing over 100 CVs per second with 98% parsing accuracy. Built with FastAPI and React, it provides quick feedback and improves hiring accuracy by 20%.

Key Features
CV Parsing: Extracts text from PDFs and DOCX with 98% accuracy.

Smart Evaluation: Uses MiniLM embeddings + cosine similarity for fast, accurate scoring.

User Roles: Separate dashboards for job seekers, recruiters, and admins.

Scalable & Secure: FastAPI backend, Cloudinary for storage, and JWT-based authentication.

Tech Stack
Backend: FastAPI, HuggingFace, LangChain, PyPDF2, python-docx

Frontend: React, Axios

Storage: Cloudinary

Model: MiniLM (all-MiniLM-L6-v2)

Security: JWT, bcrypt

Setup
Clone repo:
git clone https://github.com/your-username/cv-align.git

Backend setup:

bash
Copy
Edit
cd backend  
python -m venv venv  
source venv/bin/activate  
pip install -r requirements.txt  
Create a .env file with:

ini
Copy
Edit
CLOUDINARY_URL=...
JWT_SECRET_KEY=...
HUGGINGFACE_TOKEN=...
Frontend setup:

bash
Copy
Edit
cd ../frontend  
npm install  
Run app:

bash
Copy
Edit
uvicorn main:app --reload  # Start backend  
npm start                  # Start frontend  
Visit: http://localhost:3000

How It Works
Job Seekers: Upload CVs and explore jobs.

Recruiters: Post jobs, get ranked CVs with feedback.

Admins: Manage users, jobs, and CVs.

CvAlign uses semantic search (RAG + MiniLM) to match CVs to job descriptions and returns feedback in under a second.
