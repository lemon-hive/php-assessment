# 💼 PHP Intern Task – Blog CMS (Tailwind + OOP PHP + MySQL)

📬 **Submission:** Share your GitHub repo link via email

---

## 🎨 Frontend Guidelines

- ✅ Use **SCSS** for styling.
- ✅ Prefix classes with `lh-`, e.g., `lh-hero-banner`.
- ✅ Design using a **mobile-first** approach.
- ✅ Ensure **cross-browser compatibility**.
- ✅ Use **semantic HTML** elements.
- ✅ Apply **ARIA properties** where necessary.
- ✅ Follow the **DRY (Don’t Repeat Yourself)** principle.

## ✅ Task 1 – Blog List Page (`index.php`)

### 📌 Display:
- 🖼️ **Featured image**  
- 📝 **Title**  
- ✂️ **Short description** (truncate content)  
- 🔗 **“Read More” button** linking to full post  
- 📄 **Pagination** (5 or 10 posts per page)
- ⚙️ Posts Per Page: Admin can configure how many posts appear per page from the admin panel

---

## ✅ Task 2 – Single Blog Page (`blog.php`)

### 📌 Display:
- 📝 **Full blog title**  
- 🖼️ **Featured image**  
- 📖 **Full description/content**

---

## ✅ Task 3 – Admin Panel (`/admin` folder)

### 📌 Pages:
- 🔐 **Login:** Hardcoded credential check (user: lemon, password: lemon)
- 📋 **Dashboard:** List blog posts with **Edit/Delete** options  
- ➕ **Create Post:** Form with `title`, `description`, and `image` (jpg/jpeg/png only)  
- ✏️ **Edit Post:** Pre-filled form to update post  
- ❌ Delete with Confirmation (AJAX):

    - Show a modal or prompt before deletion

    - On confirmation, delete the post via AJAX (no page reload)

    - On success, remove the post from the list without refreshing
- ⚙️ Settings Page: Set the number of blog posts to show per page on the frontend

---

## ✅ Backend Requirements (PHP OOP + MySQL)

### 📦 Structure:
- ⚙️ Use **pure PHP** (no frameworks)
- 🧱 Organize code with **namespaces** (e.g., `App\Models`, `App\Controllers`)
- 🧩 Use **reusable classes** (e.g., `Database`, `Blog`, `RequestHandler`)

---

## 🛢️ Database

### 📌 Table: `blogs`
| Field        | Type                               |
|--------------|------------------------------------|
| `id`         | INT PRIMARY KEY AUTO_INCREMENT     |
| `title`      | VARCHAR(255)                       |
| `description`| TEXT                               |
| `image`      | VARCHAR(255)                       |
| `created_at` | TIMESTAMP DEFAULT CURRENT_TIMESTAMP|

---

## 📁 Image Upload

- 🗂️ Save images to `uploads/` folder  
- 📝 Rename files to: `filename_timestamp.ext`  
  - _Example_: `banner.jpg` → `banner_20250507123045.jpg`  
- ✅ Validate file type: **jpg**, **jpeg**, or **png**

---

## 🧠 Core PHP Classes

- **Database**  
  - Singleton PDO connection

- **Blog**  
  - `getAll($limit, $offset)`  
  - `getById($id)`  
  - `create($title, $desc, $img)`  
  - `update($id, $title, $desc, $img)`  
  - `delete($id)`

---

### 📎 Reminder:
Make sure your final GitHub repo is:
- 📁 Well structured
- 📸 Includes sample images
- 📜 Has a working demo (if possible)

---

Good luck! 🚀
