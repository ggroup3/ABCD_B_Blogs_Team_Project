### README for ABCD Project

---

## Project Overview

The ABCD Project is a photo blogging platform designed by Team Bears. It allows users to create, manage, and explore blogs, with tailored functionalities for visitors, registered users, and administrators.
---

## Features

### Visitor View
- **Browse Blogs**: Visitors can explore blogs on the main page using filters or by viewing user profiles.
- **Login or Registration**:
  - **Login**: Requires email and password.
  - **Sign Up**: Requires first name, last name, email, and password.

### Registered User Dashboard
- **User Blogs**:
  - View and manage personal blogs and summaries.
  - Create blogs with options to upload images and make them public.
- **Search and Filter**:
  - Sort blogs by:
    - Alphabetical order (normal or reverse)
    - Chronological order (normal or reverse)
- **Alphabet Book**: Generate a printable alphabet book from blog content.

### Admin Dashboard
- **Blog Management**:
  - View, edit, or delete blogs.
  - Generate alphabet books from blog content.
- **User Management**:
  - View and delete user accounts.
- **Reporting**:
  - Filter blog and user data by category or column.
  - Generate site-wide statistics.
- **Preferences**:
  - Adjust homepage display settings.
- **Sharing**:
  - Shareable links enable direct access to blog details.

---

## Repository Structure

```
├── admin/                          # Admin-specific files and configurations
├── classes/                        # Core PHP classes
│   └── AlphabetBook.php            # Handles alphabet book creation
├── css/                            # Stylesheets for various pages
│   ├── Header.css
│   ├── blogdetail.css
│   └── ... 
├── docs/                           # Documentation
│   └── ABCD_User_Manual.pptx       # User manual
├── footerFiles/                    # Static footer content
│   ├── about_us.php
│   ├── terms_of_service.php
│   └── ... 
├── images/                         # Image assets
│   ├── default_image.jpg
│   ├── brandLogo.png
│   └── ... 
├── includes/                       # Shared PHP components
│   ├── footer.php
│   └── header.php
├── js/                             # JavaScript files
│   ├── darkmode.js
│   ├── index.js
│   └── ... 
├── scripts/                        # Server setup scripts
│   └── setup.php
├── sessionManagement/              # Session management scripts
│   ├── db_configuration.php
│   ├── functions.php
│   └── logic.php
├── videos/                         # Video assets
│   ├── blog_video_0.mp4
│   └── default_video.mp4
├── youtube/                        # YouTube-related scripts
│   └── getYoutube.php
├── (root directory)                # Main PHP files
│   ├── index.php                   # Home page
│   ├── register.php                # Registration form
│   ├── create_blog.php             # Blog creation
│   ├── admin_blogs.php             # Admin blog panel
│   ├── alphabetBook.php            # Alphabet book generation
│   └── ... 
```

---

## Installation

### Prerequisites
- PHP 7.4 or later
- MySQL or MariaDB
- Web server (e.g., Apache, Nginx)

### Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/sjasthi/photo_abcd_B.git
   cd photo_abcd_B
   ```

2. **Set up the database**:
   - Import the provided SQL scripts in `scripts/setup.php` into your database.

3. **Configure environment variables**:
   - Update `sessionManagement/db_configuration.php` with your database credentials.

4. **Install dependencies**:
   - Ensure required PHP extensions (e.g., `mysqli`, `gd`) are enabled.

5. **Run the application**:
   - Deploy the repository files to your web server’s document root.
   - Access the platform via your browser (e.g., `http://localhost/photo_abcd_B`).

---

## Usage

### Creating a Blog
1. Log in or register as a user.
2. Navigate to the "Create a New Blog" section.
3. Fill in the blog title and content.
4. (Optional) Upload an image and select the "Make Public" option.
5. Click "Post" to publish.

### Managing Users (Admin)
1. Log in as an administrator.
2. Access the "Admin Dashboard."
3. Navigate to "Users" to view or delete accounts.

### Generating an Alphabet Book
1. Go to the "Alphabet Book" section in the dashboard.
2. Select the blogs to include.
3. Click "Generate" to create a printable file.

---
Video Blog Enhancement

video blog functionality us added to the existing Photo Blog application. Blogs can now include YouTube links managed in the database.

Features

Video Mode:
Displays one video per blog, one blog per row.
Shows blog text below the video.
Admin Configuration:
Set BLOG_MODE to Video to restrict blogs to a single YouTube link.
Database Update:
Added a youtube_link column to store YouTube links.
Usage

Admin sets BLOG_MODE = Video in the admin panel.
Users create blogs by providing a YouTube link (no images allowed in this mode).
