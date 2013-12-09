# README for @jpducassou - SEO 2013 required

## Documentation bellow

### **Valid HTML/CSS (w3c validator y eXaminator)**

Done using -->
Automatic evaluation of accessibility - http://examinator.ws/
W3C Markup Validation Service - http://validator.w3.org/

### **Robots.txt**

Done typing --> Disallow: /readme.md 
I prevented the search engine robots from accessing this file.

### **Responsive Design **

Done using --> Media Queries @media in the stylesheets (.css)

### **Redirection - 301 Moved Permanently**

Done configurating --> .htaccess (Apache mod_rewrite)

> <IfModule mod_rewrite.c>
  RewriteEngine on
  RewriteCond %{HTTP_HOST} ^g07.ceophp.net$ [OR]
  RewriteCond %{HTTP_HOST} ^www.g07.ceophp.net$
  RewriteRule ^/?$ "http\:\/\/www\.ropabebe.ceophp\.net\/" [R=301,L]
  </IfModule>

### **URL canonicalization**

Done configuration --> .htaccess (Apache mod_rewrite)
Item above AND

Rewrite www.mysite.com → mysite.com
> <IfModule mod_rewrite.c>
    RewriteCond %{HTTPS} !=on
    RewriteCond %{HTTP_HOST} ^www\.(.+)$ [NC]
    RewriteRule ^ http://%1%{REQUEST_URI} [R=301,L]
  </IfModule>

### **Error Documents**

Handled configuring Apache .htaccess:
>ErrorDocument 404 /404.html
>ErrorDocument 500 /500.html

### **Speed up page load times - Better cache control**

Done configurating --> Expires headers in .htaccess (Apache mod_expires)

><IfModule mod_expires.c>

    ExpiresActive on
    ExpiresDefault                                      "access plus 1 month"

  # CSS
    ExpiresByType text/css                              "access plus 1 year"

  # Data interchange
    ExpiresByType application/json                      "access plus 0 seconds"
    ExpiresByType application/xml                       "access plus 0 seconds"
    ExpiresByType text/xml                              "access plus 0 seconds"

  # Favicon (cannot be renamed!)
    ExpiresByType image/x-icon                          "access plus 1 week"

  # HTML components (HTCs)
    ExpiresByType text/x-component                      "access plus 1 month"

  # HTML
    ExpiresByType text/html                             "access plus 0 seconds"

  # JavaScript
    ExpiresByType application/javascript                "access plus 1 year"

  # Manifest files
    ExpiresByType application/x-web-app-manifest+json   "access plus 0 seconds"
    ExpiresByType text/cache-manifest                   "access plus 0 seconds"

  # Media
    ExpiresByType audio/ogg                             "access plus 1 month"
    ExpiresByType image/gif                             "access plus 1 month"
    ExpiresByType image/jpeg                            "access plus 1 month"
    ExpiresByType image/png                             "access plus 1 month"
    ExpiresByType video/mp4                             "access plus 1 month"
    ExpiresByType video/ogg                             "access plus 1 month"
    ExpiresByType video/webm                            "access plus 1 month"

  # Web feeds
    ExpiresByType application/atom+xml                  "access plus 1 hour"
    ExpiresByType application/rss+xml                   "access plus 1 hour"

  # Web fonts
    ExpiresByType application/font-woff                 "access plus 1 month"
    ExpiresByType application/vnd.ms-fontobject         "access plus 1 month"
    ExpiresByType application/x-font-ttf                "access plus 1 month"
    ExpiresByType font/opentype                         "access plus 1 month"
    ExpiresByType image/svg+xml                         "access plus 1 month"

</IfModule>

### **Minify Resources (HTML, CSS, and JavaScript)**

Done using --> http://yui.github.io/yuicompressor/

### XML Sitemap 

(Help improve spiderability and ensure that all the important pages on my site are crawled and indexed.)

Done using --> http://gsitecrawler.com/
























