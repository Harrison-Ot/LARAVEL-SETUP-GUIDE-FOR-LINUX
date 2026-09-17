
# Laravel Setup Guide for Linux (Ubuntu)

A quick-reference cheat sheet for setting up the Laravel Installer and creating new Laravel applications via the Ubuntu terminal.

---

## 🛠️ Step 1: Check or Fix the Laravel Installer

To verify if the Laravel installer is globally accessible on your system, run:
```bash
laravel --version
```

### 🔍 Fixing "Command Not Found" (Ubuntu)
If the system cannot find the `laravel` command, the global Composer binaries need to be added to your system's `PATH`. Run these two commands:

```bash
# 1. Append the Composer binary path to your .bashrc file
echo 'export PATH="HOME/.config/composer/vendor/bin:PATH"' >> ~/.bashrc

# 2. Apply the changes immediately to your current terminal session
source ~/.bashrc
```

---

## 🚀 Step 2: Creating a New Laravel Project

You can create a project using either the global Laravel installer or directly through Composer.

### Option A: Using the Laravel Installer
Once the installer is verified above, create a project instantly by running:
```bash
laravel new my-laravel-app
```

### Option B: Using Composer Directly
If you prefer not to use the global installer, use Composer to fetch the project structure:
```bash
composer create-project laravel/laravel my-laravel-app
```

---

## 🏃‍♂️ Step 3: Running the Application

After generating your project, navigate into the directory and spin up the local development server:

```bash
# Move into the project directory
cd my-laravel-app

# Start the built-in development server
php artisan serve
```

Open your browser and navigate to: **`http://127.0.0.1:8000`**

