## 1.15.26 2022-01-07 <dave at tiredofit dot ca>

   ### Added
      - Rebuild image to support base level updates, sepcifically to allow MySQL 5.7 to operate


## 1.15.25 2022-01-05 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.27


## 1.15.24 2021-12-31 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.26


## 1.15.23 2021-12-26 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.25


## 1.15.22 2021-12-13 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.24


## 1.15.21 2021-12-03 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.23


## 1.15.20 2021-11-30 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.22

   ### Changed
      - Fix to artisan alias command


## 1.15.19 2021-11-15 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.21


## 1.15.18 2021-10-21 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.20


## 1.15.17 2021-10-20 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.19


## 1.15.16 2021-10-14 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.18


## 1.15.15 2021-09-23 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.17


## 1.15.14 2021-09-19 <dave at tiredofit dot ca>

   ### Changed
      - Update artisan to remember previous directory


## 1.15.13 2021-08-25 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.16


## 1.15.12 2021-08-11 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.15


## 1.15.11 2021-08-03 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.14


## 1.15.10 2021-07-24 <dave at tiredofit dot ca>

   ### Changed
      - Restore missing "defaults" file which was causing installations not explictly setting DB_PORT to have databases wiped out
      - Quiet down installation routines that were showing database passwords unneccessarily


## 1.15.9 2021-07-22 <dave at tiredofit dot ca>

   ### Changed
      - Fix in 1.15.8 that wiped existing installations databases (!)


## 1.15.8 2021-07-20 <dave at tiredofit dot ca>

   ### Changed
      - Change the way the scheduler gets added into system timers
      - Correctly set Timezone when running scheduler


## 1.15.7 2021-07-19 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.13


## 1.15.6 2021-07-11 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.12


## 1.15.5 2021-06-23 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.11


## 1.15.4 2021-06-16 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.10


## 1.15.3 2021-05-21 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.9


## 1.15.2 2021-05-19 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.7


## 1.15.1 2021-05-14 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.6


## 1.15.0 2021-05-11 <dave at tiredofit dot ca>

   ### Added
      - Stop requiring ADMIN_EMAIL and ADMIN_PASS to be set after installation
      - Allow SETUP_TYPE=MANAL to bypass any in place variable/setup checks


## 1.14.4 2021-05-11 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.5


## 1.14.3 2021-04-23 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.4


## 1.14.2 2021-04-22 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.3
      - Support new tiredofit/nginx-php-fpm base


## 1.14.1 2021-04-20 <dave at tiredofit dot ca>

   ### Changed
      - Preload Iconv for PHP8 not PHP7


## 1.14.0 2021-04-15 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.7.2
      - PHP 8.x


## 1.13.3 2021-03-17 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.20


## 1.13.2 2021-03-14 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.19


## 1.13.1 2021-03-09 <dave at tiredofit dot ca>

   ### Added
      - Enable PHP gnuPG extensiont to support new encrypted mail module


## 1.13.0 2021-03-08 <detrepo@github>

   ### Added
      - DB Port checking for new installs to avoid overwriting the databse


## 1.12.11 2021-03-07 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.18


## 1.12.10 2021-03-03 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.17


## 1.12.9 2021-02-25 <dave at tiredofit dot ca>

   ### Added
      - Switch to PHP 7.4 Base


## 1.12.8 2021-02-25 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.16


## 1.12.7 2021-02-13 <dave at tiredofit dot ca>

   ### Fixed
      - Fix for 1.12.6

## 1.12.6 2021-02-13 <kometchtech@github>

   ### Fixed
      - Fix for Laravel/Freescout log files not saving properly

## 1.12.5 2021-02-13 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.15


## 1.12.4 2021-02-10 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.14


## 1.12.3 2021-01-16 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.13


## 1.12.2 2021-01-08 <dave at tiredofit dot ca>

   ### Changed
      - Revert to PHP 7.3 due to incompatibilities with the LDAP Module


## 1.12.1 2021-01-04 <dave at tiredofit dot ca>

   ### Reverted
      - Revert Change to Scheduler back to cron


## 1.12.0 2020-12-31 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.12

   ### Changed
      - Change the way that artisan schedule command works. Instead of running through cron, use a seperate S6 process to control.


## 1.11.2 2020-12-24 <dave at tiredofit dot ca>

   ### Added
      - Freescoutt 1.6.11


## 1.11.1 2020-12-17 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.10


## 1.11.0 2020-12-12 <dave at tiredofit dot ca>

   ### Added
      - Switch to PHP 7.4

## 1.10.15 2020-12-03 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.9


## 1.10.14 2020-11-26 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.8


## 1.10.13 2020-11-07 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.7


## 1.10.12 2020-10-31 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.6


## 1.10.11 2020-10-28 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.5


## 1.10.10 2020-10-27 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.4


## 1.10.9 2020-10-26 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.3


## 1.10.8 2020-10-06 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.2


## 1.10.7 2020-10-02 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.1


## 1.10.6 2020-09-22 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.6.0

   ### Changed
      - Reduced image size by deleting install cache


## 1.10.5 2020-09-16 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.15 (support new API and Webhook Module)


## 1.10.4 2020-09-12 <dave at tiredofit dot ca>

   ### Added
      - Add additional cache clear statement


## 1.10.3 2020-09-11 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.14


## 1.10.2 2020-08-24 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.12


## 1.10.1 2020-08-23 <dave at tiredofit dot ca>

   ### Reverted
      - Removed Timezone variable - It was causing problems resetting


## 1.10.0 2020-08-23 <dave at tiredofit dot ca>

   ### Added
      - Added `SETUP_TYPE` environment variable to skip editting .env/config after first boot
      - Added additional configuration cache clear upon startup

   ### Changed
      - Changes to the way configuration is written as per shellcheck


## 1.9.0 2020-08-22 <dave at tiredofit dot ca>

   ### Added
      - Change the way we pull Freescout - Now pull from Git and allow checking out different branches and repository URLs


## 1.8.5 2020-07-26 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.11


## 1.8.4 2020-07-23 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.10


## 1.8.3 2020-07-17 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.9


## 1.8.2 2020-06-28 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.8

   ### Changed
      - Cleanup code to fix shellcheck warnings


## 1.8.1 2020-06-20 <dave at tiredofit dot ca>

   ### Changed
      - Fix for Administrative user not being created on first boot


## 1.8.0 2020-06-08 <dave at tiredofit dot ca>

   ### Added
      - Changes to support tiredofit/alpine 5.0.0 base image


## 1.7.12 2020-05-28 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.7


## 1.7.11 2020-05-16 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.6


## 1.7.10 2020-04-26 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.4


## 1.7.9 2020-03-29 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.3


## 1.7.8 2020-03-21 <dave at tiredofit dot ca>

   ### Changed
      - Cleanup configuration with the mess caused by 1.7.0 and up


## 1.7.7 2020-03-21 <dave at tiredofit dot ca>

   ### Changed
      - Fix Secure Downloads


## 1.7.6 2020-03-21 <dave at tiredofit dot ca>

   ### Changed
      - Fix Auto Upgrade routine


## 1.7.5 2020-03-19 <dave at tiredofit dot ca>

   ### Changed
      - Bugfix for Storage Attachments


## 1.7.4 2020-03-16 <dave at tiredofit dot ca>

   ### Changed
      - Fix logfile directory permissions


## 1.7.3 2020-03-13 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.2


## 1.7.2 2020-03-12 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.5.1

   ### Changed
      - Switch from using expect to create new Admin user to new command line function introduced in 1.5.1


## 1.7.1 2020-03-10 <dave at tiredofit dot ca>

   ### Changed
      - Fix to nginx configuration as per https://github.com/freescout-helpdesk/freescout/issues/522#issuecomment-596923374


## 1.7.0 2020-03-09 <dave at tiredofit dot ca>

   ### Added
      - Update to Freescout 1.5.0
      - Add new routines to migrate old public attachments to private attachments
      - Serve attachments via Nginx instead of PHP


## 1.6.13 2020-03-05 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.12


## 1.6.12 2020-02-18 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.11


## 1.6.11 2020-02-16 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.10


## 1.6.10 2020-02-09 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.9


## 1.6.9 2020-02-02 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.8


## 1.6.8 2020-01-29 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.7


## 1.6.7 2020-01-25 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.6


## 1.6.6 2020-01-24 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.4


## 1.6.5 2020-01-19 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.3


## 1.6.4 2020-01-17 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.2


## 1.6.3 2020-01-14 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.1


## 1.6.2 2020-01-07 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.4.0

## 1.6.1 2020-01-02 <dave at tiredofit dot ca>

   ### Changed
      - Additional changes to support new tiredofit/alpine base image


## 1.6.0 2019-12-29 <dave at tiredofit dot ca>

   ### Added
      - Update to support new tiredofit/alpine base image


## 1.5.8 2019-12-28 <dave at tiredofit dot ca>

   ### Added
      - FreeScout 1.3.19


## 1.5.7 2019-12-22 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.3.18


## 1.5.6 2019-12-21 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.3.17


## 1.5.5 2019-12-18 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.3.16


## 1.5.4 2019-12-18 <dave at tiredofit dot ca>

   ### Changed
      - Dynamically set Nginx User and Group permissions across project


## 1.5.3 2019-12-17 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.3.15


## 1.5.2 2019-12-17 <dave at tiredofit dot ca>

   ### Changed
      - Cleanup Dockerfile


## 1.5.1 2019-12-15 <dave at tiredofit dot ca>

   ### Changed
      - Bugfixes to initialization script


## 1.5.0 2019-12-13 <dave at tiredofit dot ca>

   ### Added
      - Add `APPLICATION_NAME` to support changing name from Freescout to something custom


## 1.4.4 2019-12-12 <dave at tiredofit dot ca>

   ### Changed
      - Final tweak to running database migrations on startup


## 1.4.3 2019-12-12 <dave at tiredofit dot ca>

   ### Changed
      - Change in the way that DB Migrations are done. Do them every time to avoid any uncaught module installations


## 1.4.2 2019-12-11 <dave at tiredofit dot ca>

   ### Added
      - Add alias for running artisan - Type `artisan <arguments>` inside of container to run commands as webserver user


## 1.4.1 2019-12-11 <dave at tiredofit dot ca>

   ### Changed
      - Quiet down Module installation output


## 1.4.0 2019-12-11 <dave at tiredofit dot ca>

   ### Added
      - Add execution of custom scripts upon container startup (map /assets/custom-scripts)

   ### Changed
      - Fixed error where Module installation would hang


## 1.3.0 2019-12-10 <dave at tiredofit dot ca>

   ### Added
      - Refinements to Persistent Storage specifically Modules and Configuration Files
   
   ### Changed
      - Considerable cleanup related to storage
      - Automatically install Modules and clear cache routines
      - Much easier to survive container restarts
      - Fix related to auto upgrade routines


## 1.2.0 2019-12-09 <dave at tiredofit dot ca>

   ### Added
      - Refactor to support new tiredofit/nginx-php-fpm base image
      - Freescout 1.3.14


## 1.1.2 2019-11-25 <dave at tiredofit dot ca>

   ### Added
      - Freescout 1.3.12


## 1.1.1 2019-11-20 <dave at tiredofit dot ca>

   ### Added
      - Make modules persistent via new functionality introduced in 1.1.0


## 1.1.0 2019-11-20 <dave at tiredofit dot ca>

   ### Added
      - Added persistent storage for sessions, cache, and vars - Mount /data as a volume to benefit

   ### Changed
      - Updated docker-compose examples


## 1.0.4 2019-11-17 <dave at tiredofit dot ca>

   ### Changed
      - Update to Freescout 1.3.11


## 1.0.3 2019-11-11 <dave at tiredofit dot ca>

* Freescout 1.3.10

## 1.0.2 2019-10-23 <dave at tiredofit dot ca>

* Freescout 1.3.8

## 1.0.1 2019-09-10 <dave at tiredofit dot ca>

* Freescout 1.3.6

## 1.0 2019-08-08 <dave at tiredofit dot ca> w/ help from <briangilbert@github>

* Freescout 1.3.5
* Ability to Self Update
* Auto upgrade from Image version to image version
* Ability to add custom modules
* Ability to have access to custom source (this should allow Auto Updating to work without having to always update the image)
* Moved back to tiredofit/nginx-php-fpm base image to make development and upkeep easier
* PHP 7.3

## 0.11 2019-07-31 <dave at tiredofit dot ca>

* Freescout 1.3.3

## 0.10 2019-07-07 <dave at tiredofit dot ca>

* Freescout 1.2.4

## 0.9 2019-04-27 <dave at tiredofit dot ca>

* Freescout 1.1.7

## 0.8 2019-04-08 <dave at tiredofit dot ca>

* Switch to Alpine Edge
* Use gnuiconv from community instead of testing

## 0.7 2019-01-03 <dave at tiredofit dot ca>

* Freescout 1.1.6

## 0.6 2018-12-21 <dave at tiredofit dot ca>

* Freescout 1.1.3

## 0.5 2018-12-10 <dave at tiredofit dot ca>

* Freescout 1.1.1

## 0.4 2018-11-27 <dave at tiredofit dot ca>

* Freescout 1.0.7

## 0.3 2018-11-06 <dave at tiredofit dot ca>

* Rebuild Image from Alpine 3.8 Base omitting previous usage of tiredofit/nginx-php-fpm
* Fix for Iconv PHP Imap Errors (really)
* Alter location for freescout logs
* Logrotate for Freescout Fetch Logs

## 0.2 2018-11-04 <dave at tiredofit dot ca>

* Add gnu-libiconv to resolve IMAP errors

## 0.1 2018-11-03 <dave at tiredofit dot ca>

* Initial Release
* Alpine 3.8
* PHP 7.2
* Freescout 1.0.0


