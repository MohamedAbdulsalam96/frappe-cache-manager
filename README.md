# Cache Manager

Cache Manager is a Frappe app that enhances the performance of your Frappe/ERPNext applications by implementing Redis caching for data retrieval functions. It supports multi-tenancy, avoids conflicts with existing Frappe Redis use cases, and is production-ready.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [License](#license)

## Features

- **Improved Performance**: Caches results of common data retrieval functions to reduce database load and improve response times.
- **Multi-Tenancy Support**: Ensures cached data is isolated per site in a multi-tenant environment.
- **No Conflicts with Frappe Redis Usage**: Uses a separate Redis database index to avoid interfering with Frappe's Redis instances (scheduler, queue, etc.).
- **Monkey Patching**: Overrides core functions to add caching without modifying Frappe's source code.
- **Robust Error Handling**: Gracefully handles exceptions and logs errors without disrupting the application.
- **Production-Ready**: Designed for deployment in production environments with proper error handling and compatibility considerations.

## Installation
```bash
bench get-app https://git.techseria.com/erpnext/cache_manager.git
bench --site your-site-name install-app cache_manager

### Prerequisites

- **Frappe Framework**: Ensure you have a working Frappe or ERPNext installation.
- **Redis Server**: A Redis server accessible to your Frappe instance.


#### License

agpl-3.0