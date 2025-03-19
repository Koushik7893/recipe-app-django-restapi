# **Recipe REST API using Django & Django REST Framework (DRF)**  

## 🌟 **Overview**  
This project is a **Django-based REST API** for managing recipes, ingredients, and tags. It allows users to:  
✅ **Create, update, and delete recipes**  
✅ **Manage ingredients and tags**  
✅ **Retrieve recipes using filters**  
✅ **Perform CRUD operations via REST APIs**  

---

## 🎯 **Features**  

### 🔹 **1. Recipe Management**  
- **Create new recipes** with name, description, ingredients, tags, and cooking instructions.  
- **Retrieve recipes** via API with filtering options.  
- **Update recipe details** such as ingredients and instructions.  
- **Delete recipes** when no longer needed.  

### 🔹 **2. Ingredient Management**  
- **Add and list ingredients** used in recipes.  
- **Update ingredient details** (e.g., quantity, type).  
- **Delete unused ingredients** from the database.  

### 🔹 **3. Tag Management**  
- **Create, list, and delete tags** to categorize recipes.  
- Tags help users filter recipes based on cuisine, meal type, or dietary restrictions.  

### 🔹 **4. REST API Endpoints**  
The API follows **RESTful principles** and provides the following endpoints:  

| **Method** | **Endpoint** | **Description** |
|------------|------------|----------------|
| `GET` | `/api/recipes/` | Get all recipes |
| `POST` | `/api/recipes/` | Create a new recipe |
| `GET` | `/api/recipes/{id}/` | Get a specific recipe |
| `PUT/PATCH` | `/api/recipes/{id}/` | Update a recipe |
| `DELETE` | `/api/recipes/{id}/` | Delete a recipe |
| `GET` | `/api/ingredients/` | Get all ingredients |
| `POST` | `/api/ingredients/` | Add a new ingredient |
| `DELETE` | `/api/ingredients/{id}/` | Delete an ingredient |
| `GET` | `/api/tags/` | Get all tags |
| `POST` | `/api/tags/` | Create a new tag |
| `DELETE` | `/api/tags/{id}/` | Delete a tag |

### 🔹 **5. Authentication & Security**  
- API access is **secured with authentication** (Token or JWT-based).  
- Users need to **log in** to create or modify recipes.  

---

## 🚀 **Tech Stack**  

- **Backend**: Django, Django REST Framework (DRF)  
- **Database**: PostgreSQL   
- **Authentication**: Django authentication system  
- **Deployment**: Docker Hub

---

## 🛠 **Setup Instructions**  

1️⃣ **Clone the Repository**  
```bash
git clone https://github.com/Koushik7893/Recipe-App-Django-Restapi.git
cd recipe-api
```

2️⃣ **Create a Virtual Environment & Install Dependencies**  
```bash
python -m venv venv
source venv/bin/activate  # (Windows: venv\Scripts\activate)
pip install -r requirements.txt
```

3️⃣ **Apply Migrations & Run Server**  
```bash
python manage.py migrate
python manage.py runserver
```

4️⃣ **Test API using Postman or cURL**  
```bash
curl -X GET http://127.0.0.1:8000/api/recipes/
```

---

## 📌 **Future Enhancements**  
✔ **User authentication with JWT**  
✔ **Recipe image upload feature**  
✔ **Recipe rating & reviews system**  
✔ **Advanced filtering & search**  

This **Django REST API** efficiently manages **recipes, ingredients, and tags**, making it a scalable solution for food-based applications. 🚀
