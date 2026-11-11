# Library & Inventory Management System

A full-stack web application for managing a library catalogue and book inventory in one place. Built with PHP and MySQL, with a responsive Bootstrap interface.

Instead of tracking books, availability, and users in separate registers or spreadsheets, the system keeps the catalogue searchable online and ties it to live inventory and role-based access.

## What the project does

The application gives a library two views of the same data:

- A catalogue that users can search to find a book quickly.
- An admin side for managing the collection and keeping inventory up to date.

Access is controlled by login and role, so day-to-day browsing and collection management do not share the same permissions.

## Key features

**Dynamic catalogue search**

- Search the book catalogue from the interface instead of scrolling a full list.
- Find titles faster when checking whether a book exists and whether it is available.

**Role-based authentication**

- Separate login access for admins and regular users.
- Admins can manage the catalogue and inventory.
- Regular users get the browsing and search experience, without admin controls.

**Book issue, return and renewal requests**

- Users can request a book issue, ask for a renewal, or return a book.
- Admins review and accept or reject each request, and the inventory updates accordingly.

**Inventory and record tracking**

- Keep track of the books held in the library as stock changes.
- Issue, return and renewal records are stored, so a search result reflects what the library actually holds.

**Messages and recommendations**

- Users can send messages to the admin and recommend books for the library.
- Admins can read and reply to messages from the dashboard.

## Tech stack

| Layer | Technologies |
| --- | --- |
| Front end | HTML5, CSS3, JavaScript, Bootstrap |
| Back end | PHP |
| Database | MySQL |
| Interface | Responsive, browser-based |

## Project structure

```
├── index.php          # Login landing page
├── dbconn.php         # MySQL connection (localhost defaults)
├── see.php            # Book details view
├── terms.html         # Terms page
├── admin/             # Admin dashboard: books, users, issue/return/renew requests
├── student/           # User side: catalogue search, requests, profile
├── database/          # MySQL dumps for all tables (database name: LMS)
├── css/               # Shared styles
└── images/            # Shared images
```

## Getting started

The project runs locally on a standard PHP and MySQL setup, such as XAMPP on Windows.

1. Install XAMPP and start the Apache and MySQL services.
2. Copy this project folder into the XAMPP `htdocs` folder.
3. Open phpMyAdmin, create a database named `LMS`, and import the eight `.sql` files from the `database/` folder (`LMS_author`, `LMS_book`, `LMS_message`, `LMS_recommendations`, `LMS_record`, `LMS_renew`, `LMS_return`, `LMS_user`).
4. Check `dbconn.php` — it connects to `localhost` with username `root` and no password, which matches a default XAMPP install. Change these values if your MySQL setup is different.
5. Open the project in your browser through `localhost` and log in.

## Skills demonstrated

This project is the main full-stack project in my portfolio. It demonstrates:

- Building a complete web application end to end, from page layout to database.
- Writing PHP to handle server-side logic and connect pages to a MySQL database.
- Designing role-based access, with different capabilities for admins and users.
- Building search and inventory features that work on the same underlying data.
- Creating a responsive interface with HTML5, CSS3, JavaScript, and Bootstrap.

## Talking points for applications and interviews

- **Why PHP and MySQL:** a widely used, practical stack for catalogue and record-management applications, with the database doing the heavy lifting for search and inventory.
- **Hardest part to get right:** keeping catalogue search and inventory in sync, so what a user finds is what the library actually holds.
- **What role-based access taught me:** authentication is not just a login page — different users need different controls, and admin actions should never be exposed to regular users.

## Planned improvements

These are next steps, not features in the current version:

- Add a live demo and screenshots so recruiters can see the interface without installing the project.
- Add filters to catalogue search, such as by author or category.
- Improve form validation messages and empty-state messages for search results with no matches.

## Author

Sartaj Singh — BCA graduate, Gujranwala Guru Nanak Institute of Management and Technology (GGNIMT), Ludhiana, Punjab Technical University, 2024.

Built as a portfolio project for full-stack web developer roles.
