# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2025-11-23

### 🚀 Added
- **OTA Update Engine:** Implemented a fully functional Over-the-Air update system. Admins can now download and install system updates directly from the dashboard.
- **UpdateStatusCard:** Added a new component in the Admin Dashboard to visualize the current version, check for remote updates, and display the update progress.
- **Version History:** Added a direct link to this `CHANGELOG.md` file from the Admin Panel.
- **Database Logging:** System updates are now logged into the `gs_logs` table with the administrator's ID and IP address.

### 🛠 Changed
- **Database Schema:** Refactored `gs_game_categories` table to `gs_categories` for better naming conventions.
- **Dashboard API:** Optimized `dashboard.php` to use `LEFT JOIN` for fetching category names instead of relying on separate queries.
- **Version Control:** Moved version tracking from `version.json` file to the database (`gs_settings` table) for better persistence.

### 🐛 Fixed
- **Hydration Errors:** Resolved React hydration mismatches in the Admin Dashboard caused by date formatting and Ant Design modals.
- **PHP 500 Errors:** Fixed fatal errors in `dashboard.php` and `start-update.php` related to output buffering and UUID generation conflicts.
- **Cache Issues:** Implemented cache-busting for GitHub raw content requests to ensure the latest update information is always fetched.

---

## [1.0.0] - 2025-11-01

### 🎉 Initial Release
- **Core System:** Initial release of the Game Portal platform.
- **Authentication:** Complete user registration, login, and role-based access control (Admin/User).
- **Game Management:** Ability to list, add, edit, and delete games.
- **Admin Dashboard:** Basic statistics (Total Users, Total Games, Active Games).
- **Traffic Monitoring:** Integrated visitor logging and traffic charts.
- **Security:** Implemented secure password hashing and session management.
