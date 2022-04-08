# Remove .php .html .htm extensions from URL with .htaccess

EN: If you want to remove `.php` extension from URL, use this snippet on your `.htaccess` file.<br>
FR: Si vous souhaitez enlever le `.php` de l'URL vous pouvez utiliser cet extrait sur le fichier `.htaccess`.<br>

```
# Remove .php
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^([^\.]+)$ $1.php [NC,L]
```

EN: If you want to remove `.html` extension from URL, use this snippet on your `.htaccess` file.<br>
FR: Si vous souhaitez enlever le `.html` de l'URL vous pouvez utiliser cet extrait sur le fichier `.htaccess`.<br>

```
# Remove .html
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^([^\.]+)$ $1.html [NC, L]
```

EN: If you want to remove both `.php` and `.html`, the solution would be to rename the `.html` files to `.php` and use the first snippet.<br>
FR: Si vous souhaitez enlever à la fois `.php` et `.html`, la solution serait de renommer les fichiers `.html` en `.php` et utiliser le premier extrait.<br>
<br>
<br>

You can buy me a coffee [here](https://www.buymeacoffee.com/rasolofonirina).