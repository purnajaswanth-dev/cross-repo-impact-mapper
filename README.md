# Cross-Repo Dependency Impact Mapper

Analyzes how upgrading a shared dependency impacts multiple repositories across a system.

---

## 🚨 Problem

In large-scale systems with multiple repositories:

- Teams don’t know which services depend on a shared library  
- Upgrading a dependency can break multiple services unexpectedly  
- There is no centralized visibility into cross-repo impact  

This leads to risky deployments and production failures.

---

## 💡 Solution

This application indexes multiple GitHub repositories, extracts their dependencies, and builds a cross-repo dependency map to predict the impact of upgrading any library.

---

## 🔍 Impact Analysis

Given a dependency upgrade, the system classifies affected repositories as:

- 🔴 BREAKING  
  Major version change → high risk of API incompatibility  

- 🟡 WARNING  
  Large version gap or outdated dependency  

- 🟢 SAFE  
  Minor or patch upgrade → low risk  

---

## ⚙️ Key Features

- GitHub API integration for repository indexing  
- Automatic detection of dependency files (Maven / NPM)  
- Dependency extraction and storage  
- Cross-repository dependency mapping  
- Impact analysis engine based on semantic versioning  
- Interactive dependency graph visualization  

---

## 🧠 How It Works

1. Add GitHub repositories  
2. System fetches dependency files (`pom.xml` / `package.json`)  
3. Extracts dependencies and stores them  
4. Builds relationships between repositories based on shared libraries  
5. User inputs a dependency upgrade  
6. System predicts impact across all repositories  

---

## 🛠 Tech Stack

- Spring Boot  
- MySQL  
- GitHub REST API  
- D3.js (graph visualization)  

---

## 📌 Use Cases

- Microservices dependency management  
- Safe library upgrades  
- Pre-release impact analysis  
- Engineering productivity tools  

---

## ▶️ Running the Application

1. Add your GitHub token in `application.properties`  
2. Run the Spring Boot application  
3. Open `http://localhost:8080`  
4. Index repositories and analyze impact  

---

## ⚠️ Note

- GitHub API rate limits apply  
- Only public repositories are indexed without additional permissions  
- Sensitive credentials are not included in this repository
