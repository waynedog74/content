---
Title: "New GIS Features in MySQL 5.7"
Date: 2017-12-20 10:47:59
Categories: [data base]
tags: [mysql, mariadb, percona]
Authors: sedlav
---

MySQL 5.7 introduces the following major improvements and features for GIS:

* **Spatial indexes for InnoDB**. Finally it is here! This was a long overdue feature, which also prevented * many companies from converting all tables to InnoDB.
* **st_distance_sphere:** native function to calculate a distance between two points on earth. Finally it is * here as well! Like many others, I’ve created my stored procedure to calculate the distance between points * on earth using haversine formula. The native function is ~20x faster than the stored procedure (in an * artificial benchmark, see below). This is not surprising, as stored procedures are slow computationally – * especially for trigonometrical functions.
* **New functions:** GeoHash and GeoJSON. With GeoJSON we can generate the results that are ready for * visualizing on Google Maps.
* **New GIS** implementation based on Boost.Geometry library. This is great news, as originally GIS was * implemented independently from scratch with a very limited set of features. Manyi Lu from MySQL server * team provides more reasoning behind the choice of Boost.Geometry.


[Link](https://www.percona.com/blog/2016/02/03/new-gis-features-in-mysql-5-7/)
