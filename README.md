# Build php docker file

   docker build --no-cache -t silvermoonframework/php-7.4:latest .
   docker push silvermoonframework/php-7.4:latest
   
# Build php xdebug docker file

   docker build --no-cache -t silvermoonframework/php-7.4-xdebug:latest .
   docker push silvermoonframework/php-7.4-xdebug:latest

# Build php 8 docker file

   docker build --no-cache -t silvermoonframework/php-8.0:latest .
   docker push silvermoonframework/php-8.0:latest
