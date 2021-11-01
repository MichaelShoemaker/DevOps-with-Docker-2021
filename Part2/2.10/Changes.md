Changed 
ENV REQUEST_ORIGIN=http://frontend:5000

to

ENV REQUEST_ORIGIN=http://localhost


Had to use docker-compose stop instead of docker-compose down to get the images rebuilt correctly.
