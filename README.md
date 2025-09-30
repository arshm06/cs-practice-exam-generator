# AI-Generated Practice Test Platform (590 Final Project)

This project is a **full-stack web application** that helps students, TAs, and professors generate **course-specific practice tests** using **Generative AI**. The platform integrates uploaded course resources (PDFs, slides, notes) with GPT-powered generation to create tailored, exam-relevant practice problems and tests.  

Built for UNC’s **Computer Science Experience Labs (CSXL)**, this project is designed to provide students with a more personalized and interactive way to study for exams.

---

## Key Features

- **AI-Generated Practice Tests**  
  Input a custom prompt and select course resources to generate relevant practice tests and problems.  
- **Resource Integration**  
  Stores course PDFs, notes, and other materials in a SQL database, ensuring generated tests are grounded in actual course content.  
- **Dynamic Test Formats**  
  Choose multiple test formats (MCQ, short answer, coding problems, etc.), appended automatically to AI prompts.  
- **PDF Generation & Preview**  
  Tests are rendered to LaTeX → PDF, displayed in-browser, and downloadable.  
- **Persistent Storage**  
  Generated tests are stored in the database with unique IDs, linked to courses for retrieval and review.  
- **Drag & Drop File Uploads**  
  Upload and manage course resources through a clean Angular interface.  
- **Scalable Deployment**  
  Containerized using **Docker**, deployed via **OKD/OpenShift**.  

---

## Architecture

- **Frontend**: Angular 17+ (modern Signals API, reactive forms, modular components for input/selection/results)  
- **Backend**: FastAPI (Python) with clear separation of services, exception handling, and GPT integration  
- **Database**: PostgreSQL storing both resources (as binary PDFs) and generated tests (IDs, summaries, associations)  
- **AI Layer**: GPT-powered text generation with appended instructions for resource grounding and test formatting  
- **Deployment**: Dockerized services orchestrated via OKD (OpenShift)  

---

## User Stories

- **Students**: Generate personalized practice tests from selected course resources.  
- **TAs**: Upload curated materials and review AI-generated content.  
- **Professors**: Create official practice exams or supplemental problems.  
- **Admins**: Manage course data, resources, and permissions.  

---

## Development Timeline

We followed a **4-sprint structure**:

- **Sprint 0**: Project setup, low-fidelity wireframes, persona mapping.  
- **Sprint 1**: SQL database with preloaded resources; backend GET/DELETE APIs for resources.  
- **Sprint 2**: Frontend integration — practice test generation flow with resource selection and prompt entry.  
- **Sprint 3**: PDF rendering, storage of generated tests with unique IDs, downloadable test previews.  
- **Sprint 4**: Polishing UI/UX, error handling, Dockerization, and final deployment.  

---

