# Sitemap-generator

this is a Sitemap generator 

Python Site Map Generator uses python multi-threaded approach to read all links accessible through the Web site and generate proper
sitemap for SEO purposes. Script was meant to use threading technology to allow easy and very fast approach while generating sitemaps for your Web pages.
The script will run under Linux operating system which supports Python 3 language.


Usage example:

    mkdir pg-data
    ~/Documents/docker_files/postgres_docker$ ll
        docker.compose.yaml
        pg-data

    sudo docker-compose up -d
    sudo docker ps:
    

    CONTAINER ID        IMAGE                         COMMAND                  CREATED             STATUS              PORTS                     NAMES
    ce212aa805bb        driver220v/sitemap:improved   "sleep 50000"            2 minutes ago       Up 2 minutes                                  sitemap
    55ee61e40217        postgres:12                   "docker-entrypoint.s…"   About an hour ago   Up 2 minutes        0.0.0.0:54320->5432/tcp   postgres

- sudo docker exec -it ce212aa805bb /bin/bash


    root@ce212aa805bb:/# 
   
cd home/sitemap


    python3 main.py 'https://scrapethissite.com/'
    
python output(traverse breadth):

    https://scrapethissite.com/
    https://scrapethissite.com/pages/
    https://scrapethissite.com/lessons/
    https://scrapethissite.com/faq/
    https://scrapethissite.com/login/
    https://scrapethissite.com/pages/simple/
    https://scrapethissite.com/pages/forms/
    https://scrapethissite.com/pages/ajax-javascript/
    https://scrapethissite.com/pages/frames/
    https://scrapethissite.com/pages/advanced/
    https://scrapethissite.com/robots.txt

PostgreSQL database output(check if necessary):
    
    psql -h localhost -p 54320 -U admin -d sitemap_db
    password=docker

    sitema_db=# select * from urls;
        Url_parent                    url_children
      https://proxy-seller.ru/      | {https://proxy-seller.ru/page/rules,https://proxy-seller.ru/faq,https://proxy-seller.ru/otzyvy,https://proxy-seller.ru/blog,https://proxy-seller.ru/contacts,https://proxy-seller.ru/affiliate-program-main,https://proxy-seller.ru/authorization,https://proxy-youla,https://proxy-seller.ru/ipv6,https://proxy-seller.ru/mobile-proxies,https://proxy-seller.ru/offer,https://proxy-seller.ru/privacy-policy}

   
