**REQUIRES THE CODEIGNITER FRAMEWORK**

This class allows any table, and any type of system, to add, edit, and delete tags from any object/row without interfering with other tables that are also using tags.

For example, say you have 58 articles on your blog and each have 2-4 tags attached to them. Now you add a "Image Gallery" to your site to showoff your photos. You want to "tag" each photo with some key words (city, dark, night) that will help people sort through all the images. With this class both your blog articles and your images (and any other tables you add) can use the same "tags" table without interfering with each other.

Just because blog article 23 has the tag "sports" doesn't mean that image 23 will return the tag "sports".


About the variables this class uses:
(the fictitious tables "posts" and "images" used for examples)

TABLE
The name of a table using tags (i.e. "posts", "images", etc..)
this allows us to tell the difference between a tag for row
23 of the "images" table and row 23 of the "posts" table.

ROW\_ID
The row\_id is the unique ID of a row from the table set in TABLE.
This id corasponds to a some row like "row 23" of the "posts" table.

USER\_ID
The ID of the user that created the tag. (for use with a "users" table)
This means that multiple users can each tag a TABLE row with their own
tags. This is optional so if you don't plan on starting another social site you don't even need to use this variable.

SAFE\_TAG
This is a URL/file/etc. safe version of the TAG. (only [a-z0-9_])_

TAG
A cleaned (alphanumeric and spaces) catialized tag (only for display)

TAG\_ID
The Unique Id of the tag

DATE
The date the tag was attached to a row



Note: the bottom of the CXTags Model has the SQL for the tables you will need to add to your DB.


---


**UPDATE**
As of March 29, 2009 the SVN repo is now behind the actual releases of CXTags. The new version 2.0 can be downloaded from the downloads section.