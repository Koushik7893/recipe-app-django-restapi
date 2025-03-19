# **Recipe REST API using Django & Django REST Framework (DRF)**  

## 🌟 **Overview**  
This project is a **Django-based REST API** for managing recipes, ingredients, and tags. It is built using **Django REST Framework (DRF)** and includes authentication, Docker support, and environment configuration.  

📌 **API Documentation is available at** `/api/docs/` using **Swagger UI**.  

Users must **authenticate with a token** to perform CRUD operations on **recipes, ingredients, and tags**.  

---

## 🎯 **Features**  

### 🔹 **1. API Documentation (Swagger UI)**  
- View and test API endpoints at **`/api/docs/`**.  
- Supports authentication for testing secured routes.  

### 🔹 **2. User Authentication**  
- Users must **log in and obtain an authentication token** to access the API.  
- Admin users can log in via **Django Admin Panel**.  

### 🔹 **3. Recipe Management**  
- **Create, update, delete, and retrieve recipes**.  
- Each recipe contains **name, ingredients, tags, and instructions**.  

### 🔹 **4. Ingredient Management**  
- **Add, update, and delete ingredients** used in recipes.  

### 🔹 **5. Tag Management**  
- **Create, update, and delete tags** for categorizing recipes.  

### 🔹 **6. REST API Endpoints**  

| **Method** | **Endpoint** | **Description** |
|------------|------------|----------------|
| `POST` | `/api/user/token/` | Obtain auth token |
| `POST` | `/api/user/create/` | Create a new user |
| `GET` | `/api/recipes/` | Get all recipes |
| `POST` | `/api/recipes/` | Create a new recipe (Auth required) |
| `GET` | `/api/recipes/{id}/` | Get a specific recipe |
| `PUT/PATCH` | `/api/recipes/{id}/` | Update a recipe |
| `DELETE` | `/api/recipes/{id}/` | Delete a recipe |
| `GET` | `/api/ingredients/` | Get all ingredients |
| `POST` | `/api/ingredients/` | Add a new ingredient |
| `DELETE` | `/api/ingredients/{id}/` | Delete an ingredient |
| `GET` | `/api/tags/` | Get all tags |
| `POST` | `/api/tags/` | Create a new tag |
| `DELETE` | `/api/tags/{id}/` | Delete a tag |
| `GET` | `/api/docs/` | Access API Documentation (Swagger UI) |

### 🔹 **7. Django Admin Panel**  
- **Login via Django Admin** (`/admin/`) to manage users, recipes, and ingredients.  

---

## 🛠 **Setup Instructions**  

### ✅ **1. Clone the Repository**  
```bash
git clone https://github.com/Koushik7893/Recipe-App-Django-Restapi.git
cd Recipe-App-Django-Restapi
```

### ✅ **2. Create `.env` File**  
- Copy `.env.sample` and rename it to `.env`.  
- Modify it based on your local setup.  

### ✅ **3. Run with Docker (Development Mode)**  

1️⃣ **Run Migrations**  
```bash
docker compose run --rm app sh -c "python manage.py makemigrations"
docker compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"
```

2️⃣ **Create a Superuser**  
```bash
docker compose run --rm app sh -c "python manage.py createsuperuser"
```

3️⃣ **Start the Application**  
```bash
docker-compose up
```

4️⃣ **Stop the Application**  
```bash
docker-compose down
```

---

## 🚀 **Deployment Instructions (AWS/Production)**  

1️⃣ **Stop Existing Containers**  
```bash
docker compose -f docker-compose-deploy.yml down
```

2️⃣ **Start Application in Production Mode**  
```bash
docker compose -f docker-compose-deploy.yml up
```

---

## 📌 **Future Enhancements**  
✔ **Recipe image upload**  
✔ **Recipe ratings & reviews**  
✔ **Advanced filtering & search**  

This **Django REST API** provides a **secure and scalable** way to manage **recipes, ingredients, and tags** with authentication and API documentation via **Swagger UI**. 🚀
