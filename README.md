# 🎮 GameVault – Games Inventory Management System

**GameVault** is a web-based Game Inventory Management System developed using PHP, MySQL, JavaScript, and Tailwind CSS. It allows users to manage a collection of video games by adding, viewing, updating, deleting, searching, and organizing game records.

The system features a clean and responsive interface with dark mode support, game cover image uploads, and an inventory dashboard.

## ✨ Features

- **Dashboard Overview** – Displays the total number of games, game categories, and total inventory value.
- **Add Games** – Add new games with their name, description, category, price, and optional cover image.
- **Update Games** – Edit existing game information and replace cover images.
- **Delete Games** – Remove games from the inventory.
- **Search Games** – Search games by name, description, or category.
- **Category Filter** – Filter games according to their genres or categories.
- **Game Cover Upload** – Upload game cover images in JPG, PNG, WEBP, and GIF formats.
- **Image Preview** – Preview selected images before saving.
- **Dark Mode** – Switch between light and dark themes.
- **Responsive Design** – Accessible on desktop, tablet, and mobile devices.
- **Database Integration** – Stores game information using MySQL.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| PHP | Backend development |
| MySQL | Database management |
| HTML5 | Web page structure |
| Tailwind CSS | Styling and responsive design |
| JavaScript | Interactive functionality |
| PDO | Secure database operations |

## 📂 Project Structure

```text
GameVault/
│
├── index.php          # Main application
│
├── uploads/           # Uploaded game cover images
│
└── README.md          # Project documentation
```

The `uploads/` directory is automatically created when an image is uploaded if it does not already exist.

## ⚙️ Installation and Setup

### 1. Install Requirements

Make sure you have the following installed:

- XAMPP
- PHP 8.0 or later
- MySQL
- Web browser

### 2. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/GameVault.git
```

### 3. Move the Project

Place the project folder inside your XAMPP `htdocs` directory.

```text
C:/xampp/htdocs/GameVault/
```

### 4. Create the Database

1. Start Apache and MySQL in XAMPP.
2. Open phpMyAdmin.
3. Create a database named `product_inventory`.
4. Open the SQL tab and execute the following:

```sql
CREATE TABLE games (
    game_id INT AUTO_INCREMENT PRIMARY KEY,
    game_name VARCHAR(100) NOT NULL,
    game_description VARCHAR(100),
    game_category VARCHAR(100) NOT NULL,
    price INT NOT NULL,
    image_path VARCHAR(255) DEFAULT NULL
);
```

### 5. Configure the Database

Open `index.php` and configure the database connection using your own credentials.

```php
const DB_HOST = 'localhost';
const DB_NAME = 'product_inventory';
const DB_USER = 'root';
const DB_PASS = '';
```

**Important:** Never upload actual database passwords or private credentials to a public GitHub repository. Use environment variables or another secure configuration method for production.

### 6. Run the Application

Open your browser and visit:

```text
http://localhost/GameVault/
```

You can now start managing your game inventory!

## 🖼️ Application Overview

GameVault provides a dashboard where users can:

- View all registered games.
- Monitor the total inventory value.
- See available game categories.
- Search and filter game records.
- Add, edit, and delete game entries.

## 🔒 Security Features

- PDO prepared statements for database operations.
- CSRF token validation for form submissions.
- HTML output escaping to help prevent XSS.
- Image MIME type validation.
- Randomized filenames for uploaded images.
- Maximum image upload size of 5 MB.

## 👥 Developers

**GROUP 1**

- GRANDE
- JANABON
- ESTACA
- AMPIG

## 📌 Project Purpose

GameVault was developed as a group project to demonstrate the application of web development technologies, database integration, and CRUD (Create, Read, Update, Delete) operations in building a functional inventory management system.

---

**Made with ❤️ by GROUP 1** 🎮
