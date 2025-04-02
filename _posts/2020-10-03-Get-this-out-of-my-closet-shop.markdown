---
layout: post
title:  "Get this out of my closet. Shop."
date:   2020-10-03
tags: DigitalOcean Apache2 VirtualHosts
description: Jennifer Haggerty works with virtual hosts on Apache2.
---

Recall from the first <a href="{{ site.url }}/2020/10/01/welcome-to-jekyll.html">post</a> the reason I began this blog, my best friend needed an outlet for her collection of artworks and body care supplies. Let's take a look at how I setup her <a href="http://getthisoutofmycloset.shop">website</a>.

<h2>Acquiring the domain and web space</h2>

I use <a href="https://namecheap.com">Name Cheap</a> for my domains. They're pretty cheap with a fairly easy admin dashboard. I usually get the domain then point the DNS records to <a href="https://digitalocean.com">Digital Ocean</a> (DO) where I acquire web space. DO makes it really easy to get space on the web and point your domains to their droplets, but that's a tutorial for another time, if you're interested let me know in the comments. 

<h2>Setting up the website directories</h2>

Using a droplet I already own, to keep costs down, running <a href="https://httpd.apache.org/">Apache2</a> I put one website in `/var/www/website1.com` and added `/var/www/getthisoutofmycloset.shop`. Allowed my non-root user modification permissions, `$ sudo chown -R $USER:$USER /var/www/getthisoutofmycloset.shop`, and allowed read access, `sudo chmod -R 755 /var/www`.

Next I added a file within the shop directory labeled `index.html` to show something that'll tell me the virtual hosts are working:

```html
<html>
  <head>
    <title>Get This Out of My Closet Shop</title>
  </head>
  <body>
    <h1>Success! The virtual host is working!</h1>
  </body>
</html>
```

<h2>Create the virtual hosts</h2>

Apache gives us a template that we can copy with `$ sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/getthisoutofmycloset.shop.conf` and edit to looks like this:

```conf
<VirtualHost *:80>
  ServerAdmin thejenniferhaggerty@gmail.com
  ServerName getthisoutofmycloset.shop
  ServerAlias www.getthisoutofmycloset.shop
  DocumentRoot /var/www/getthisoutofmycloset.shop
  ErrorLog ${APACHE_LOG_DIR}/error.log
  CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

Afterwards we enable the site with `$ sudo a2ensite getthisoutofmycloset.shop.conf`, restart Apache `$ sudo systemctl restart apache2`, and test the results by navigating to <a href="http://getthisoutofmycloset.shop">http://getthisoutofmycloset.shop</a>.

At the time of this writing it should show "Success! The virtual host is working!".

<h2>Next up</h2>

Installing WordPress, SSL encryption, and WooCommerce.

Thank you for reading!