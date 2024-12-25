# TD-2: Creating Tables with Spatial Columns

## 1. Create Spatial Tables (Points)

Use the following SQL command to create a table `points_of_interest` with a geometric column of type `Point`:

```sql
CREATE TABLE points_of_interest (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    location GEOMETRY(Point, 4326)
);
```

### Steps to Insert Data Using QGIS:
1. Establish a connection to your database from QGIS.
    - Right-click on **PostGIS** in the browser panel.
    - Select **New Connection** and provide the following information:
        - **Database name**
        - **Username and password**
        - **Host and port details**
2. Open the connection.
3. In the database view, double-click on the `points_of_interest` table to add it as a layer in QGIS.
4. Switch to edit mode and add points directly on the map.
5. Save changes.

### Verification:
To verify the inserted data, run the following query in your database:

```sql
SELECT * FROM points_of_interest;
```

---

## 2. Create Spatial Tables (Polygons)

To create a table `park_boundaries` with a geometric column of type `Polygon`, use the following SQL command:

```sql
CREATE TABLE park_boundaries (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    area GEOMETRY(Polygon, 4326)
);
```

### Steps:
1. Insert data into the table using QGIS, then save your changes.
2. Verify the data using the query:

```sql
SELECT * FROM park_boundaries;
```

---

## 3. Create a Spatial Table with a LineString Column

To create a table `roads` containing a spatial column of type `LineString`, use the following SQL command:

```sql
CREATE TABLE roads (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    path GEOMETRY(LineString, 4326)
);
```

### Example for Data Verification:
Run the following query to check the data:

```sql
SELECT * FROM roads;
```

---

## Resources
- [PostGIS Documentation](https://postgis.net/documentation/)
- [QGIS Documentation](https://qgis.org/en/docs/index.html)