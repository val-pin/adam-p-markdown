Extend FastDL Module introduced with #353 

1. Select "additional domains"
--* Off
--* Redirect
--* Direct access

2. Texterea Redirect Domains
--* Per default add www.default.dns
--* Need a filter for forbidden domains like with TS3 at userpanel

3. Enhance custom attributes so they support the Web Part

4. Additional management for PHP modules (CRUD)
--* examples are SSH2, CURL, Ioncube

5. Add select field "purpose"
--* two options
---* FastDL
---* PHP
--* On change display extra PHP settings and replace vhostTemplate
---* Default memory_limit
---* Default disabled_functions
---* Default disabled_classes
---* Default URL Fopen
---* Select fields for PHP Modules
----* Not Available (default)/Optional (off at any vhost create but can be activated)/Available (on at any vhost create but can be deactivated)

5. In case of FastCGI (Nginx/Apache/Hiawatha) we need fields with fpm pool storage path and pool config template