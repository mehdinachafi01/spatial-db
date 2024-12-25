# TD1: Introduction to Spatial SQL

This guide provides a detailed walkthrough for installing PostGIS and setting up your first spatial database. PostGIS is a powerful extension of PostgreSQL, enabling advanced GIS operations within a relational database system.

---

## Prerequisites
- PostgreSQL installed on your system.
- Internet access to download the necessary extensions and tools.

---

## Steps to Follow

### 1. Install PostgreSQL
- Visit the official PostgreSQL download page and select the version for your operating system (Windows, macOS, or Linux).
- Follow the installation instructions and set up PostgreSQL on your machine.
- During installation, define a password for the `postgres` user.

### 2. Install PostGIS
- During PostgreSQL installation, ensure you select all components, including the Stack Builder tool.
- Launch Stack Builder and select the PostgreSQL version you installed.
- In the application list, choose PostGIS and complete the installation following the on-screen prompts.

### 3. Create Your First Spatial Database
- Open **pgAdmin 4**, the PostgreSQL database management tool.
- Connect to the PostgreSQL server using the credentials set during installation.
- Right-click on **Databases** and select **Create > Database**.
- Assign a name to your database (e.g., `spatial_db`) and save it.
- Open the Query Tool for your database and run the following command to enable PostGIS:
  ```sql
  CREATE EXTENSION postgis;
  ```
- Verify the installation by searching for the `spatial_ref_sys` table under **Schemas > Public > Tables**.

---

## Next Steps
Once your spatial database is set up, you can move on to creating tables with spatial columns and performing GIS operations using SQL. Check out **TD2** for more details on creating spatial tables.

---

## Resources
- [PostGIS Documentation](https://postgis.net/documentation)
- [PostgreSQL Documentation](https://www.postgresql.org/docs)
