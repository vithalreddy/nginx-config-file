# nginx-config-file
NGINX config file with 404 and 500 error pages.

```
#myserver block
server {
	location / {
	listen       80;
	server_name gotapp.com www.gotapp.com *.gotapp.com;
	root /home/vithalreddy/projects/got-app;
	}
	
	error_page 404 /custom_404.html;
 
	location = /custom_404.html {
 	root /home/vithalreddy/projects/got-app;
	internal;
}	
	error_page 500 501 502 503 504 /custom_500.html;

	location = /custom_500.html {
	root /home/vithalreddy/projects/got-app;
	internal;

	}
}

```
