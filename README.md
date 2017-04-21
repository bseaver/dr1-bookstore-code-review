# Bookstore

## Epicodus Drupal Week 1 Code Review - Create a Drupal Website

#### Demonstrate Some Essential Site Building Steps in Drupal with Appropriate Git Commits

### This project utilizes:
  * Git
  * Drupal 7.54
  * MAMP for Website and MySQL Database

### Installation Notes:
  * Database, database user, site administrator and all passwords are `bookstore`.
  * Site database is stored in sites/db-backup/ and is intended to be imported into MAMP SQL `localhost:8888/phpmyadmin/`.
  * You may need to recreate in MAMP SQL the `bookstore` administrator database user and password.

## Project Plan
  * 2 basic pages - an "About", "Locations".
  * Enable Contact module. Include a Contact form with a "Contact" link in the main menu. All user roles can use the form.
  * Install the Views, Features, and the Strongarm modules.
  * Create a feature called "Site Configuration". Make the feature track the strongarm variables site_name, site_slogan, theme_default and site_frontpage.
  * Change the site's default theme, name and slogan. Make "About" the front page. Recreate Site Configuration feature.
  * Create "Book Review" custom content type and feature. Title field relabelled "Book Title", include required fields in order "Book Author", "Rating", and "Review Body".  Rating selected by menu or radio buttons.
  * Create "New Books" view in a block. Display the 3 newest book reviews as an unformatted list of linked titles with no pager.
  * Display the block. Add 4 book reviews - verify new books fill display.
  * Add "New Books" view to "Book Review" feature.
  * Create "Reviewer" role. They may edit and delete their own reviews.
  * Create a front page coupon block visible to authenticated users: "This week: use this coupon code to get 25% off on all Science Fiction!"

## Summary of Steps Used to Build this Site:

#### Initial setup

* Copy downloaded Drupal core to (Desktop for convenience) `bookstore` site folder
* Rename (to effectively remove) .gitignore
* May be needed in access controlled environments:
  * $ `chmod -R a+w sites/default`
  * Copy `project/sites/default/default.settings.php` to `project/sites/default/settings.php`
* Point MAMP web root folder to site folder, restart servers
* Open SQL page `localhost:8888/phpmyadmin/`
* Create database with collation utf8_general_ci
* Create admin user for Drupal site's internal use
* Open `localhost:8888/` for new Drupal site
* Setup: Standard, English, Database, host and port 127.0.0.1 and 8889
* Initial Site name, email, admin user, country, time zone and turn off e-mail notices for this demo
* Export MAMP hosted database:
  * Custom, SQL, All Tables (structure and data)
  * Save output to File, Compression: zipped
  * Add create database
  * Add drop table

#### Add a Slogan and 2 Pages: About and Locations
* #overlay=admin/config/system/site-information
* #overlay-context=&overlay=node/add/page
* Adjust main menu weight, add URL alias



## Copyright (c)
* 2017 Benjamin T. Seaver

## Known Bugs
* No known bugs

## Support and contact details
* None

## License
* MIT

##### End of File
