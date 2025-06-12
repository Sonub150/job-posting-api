# 🧰 Job Posting API

A RESTful API built with **Express.js** and **MongoDB** to manage job postings — create, read, update, and delete job listings.

---

## 🚀 Getting Started

### 📦 Prerequisites

- **Node.js** (v14 or later)
- **MongoDB** (Local or Atlas)
- **npm** or **yarn**

---

### 📁 Installation

```bash
git clone https://github.com/your-username/job-posting-api.git
cd job-posting-api
npm install
```

---

### ⚙️ Configuration

Ensure MongoDB is running locally or update the URI inside the code:

```js
mongoose.connect('mongodb://localhost:27017/jobPostingDB', ...)
```

---

### ▶️ Run the Server

```bash
npm start
# or
node server.js
```

---

## 📘 API Endpoints

All API routes are prefixed with `/api/jobs`

> Base URL: `http://localhost:5000/api/jobs`

---

### 🔹 1. Create a Job

- **Endpoint:** `POST /api/jobs`
- **Description:** Create a new job posting.

#### ✅ Sample Request

```json
{
  "title": "Frontend Developer",
  "company": "TechCorp",
  "location": "Remote",
  "description": "Looking for React developer",
  "requirements": ["React", "HTML", "CSS"],
  "salary": 60000
}
```

#### 🔁 Sample Response

```json
{
  "_id": "662d...eab",
  "title": "Frontend Developer",
  "company": "TechCorp",
  ...
}
```

---

### 🔄 2. Update a Job

- **Endpoint:** `PUT /api/jobs/:id`
- **Description:** Update an existing job posting.

#### ✅ Sample Request

```json
{
  "location": "New York"
}
```

#### 🔁 Sample Response

```json
{
  "_id": "...",
  "title": "Frontend Developer",
  "location": "New York",
  ...
}
```

---

### ❌ 3. Delete a Job

- **Endpoint:** `DELETE /api/jobs/:id`
- **Description:** Delete a job by ID.

#### 🔁 Sample Response

```json
{
  "message": "Job deleted successfully"
}
```

---

### 📄 4. Get All Jobs

- **Endpoint:** `GET /api/jobs`
- **Description:** Retrieve a list of all jobs.

#### 🔁 Sample Response

```json
[
  {
    "_id": "...",
    "title": "Frontend Developer",
    "company": "TechCorp",
    ...
  }
]
```

---

## 🧪 Testing the API

Use **Postman**, **Thunder Client**, or **curl**:

```bash
curl -X GET http://localhost:5000/api/jobs
```

---

## 📂 Project Structure

```
job-posting-api/
├── index.js         # Main server file
├── package.json
├── README.md
```

---

