---
title: Filters the posts array before the query takes place with posts_pre_query 
date: 2020-01-02 16:34:19
categories: [cms]
tags: [wordpress]
authors: sedlav
---

Filtering functions that require pagination information are encouraged to set the found_posts and max_num_pages properties of the WP_Query object, passed to the filter by reference. If WP_Query does not perform a database query, it will not have enough information to generate these values itself.

[Link](https://developer.wordpress.org/reference/hooks/posts_pre_query/)
