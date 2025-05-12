# 💼 PHP Intern Task – Blog CMS (Tailwind + OOP PHP + MySQL)

📬 **Submission:** Share your GitHub repo link via email

---

## 🎨 Frontend Guidelines

- ✅ Use **TailwindCSS** for styling.
- ✅ Design using a **mobile-first** approach.
- ✅ Ensure **cross-browser compatibility**.
- ✅ Use **semantic HTML** elements.
- ✅ Apply **ARIA properties** where necessary.
- ✅ Follow the **DRY (Don’t Repeat Yourself)** principle.

## ✅ Task 1 – A top navigation.

## ✅ Task 2 – Blog List Page (`index.php`).

### 📌 Display:
- 🖼️ **Featured image**  
- 📝 **Title**  
- ✂️ **Short description** (truncate content)  
- 🔗 **“Read More” button** linking to full post  
- 📄 **Pagination** (5 or 10 posts per page)
- ⚙️ Posts Per Page: Admin can configure how many posts appear per page from the admin panel

---

## ✅ Task 3 – Single Blog Page (`blog.php`)

### 📌 Display:
- 📝 **Full blog title**  
- 🖼️ **Featured image**  
- 📖 **Full description/content**

---

## ✅ Task 4 – Admin Panel (`/admin` folder)

### 📌 Pages:
- 🔐 **Login:** Hardcoded credential check (user: lemon, password: lemon)
    - If the user is not authenticated, accessing the admin panel shows a login form. The login form authenticates using hardcoded credentials (username: lemon, password: lemon). On success, store the login state in the PHP session, and skip the login form for the rest of the session.

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
⚙️ Use **pure PHP** (no frameworks)
  
🧱 Organize code with namespaces using the LH prefix (e.g., LH\Models, LH\Controllers).

🧩 Use reusable classes with the LH prefix (e.g., LH\Database, LH\Blog, LH\RequestHandler).


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

## 🧠 Core PHP Classes Examples

### LH\Database
- Singleton PDO connection

### LH\Blog
- `getAllPosts($limit, $offset)`
- `getPostById($id)`
- `createPost($title, $desc, $img)`
- `updatePost($id, $title, $desc, $img)`
- `deletePost($id)`

### LH\RequestHandler
- `getRequest($key)`
- `postRequest($key)`
- `validate($data)`


---

### 📎 Reminder:
Make sure your final GitHub repo is:
- 📁 Well structured
- 📸 Includes sample images
- 📜 Has a working demo (if possible)

---

Good luck! 🚀
