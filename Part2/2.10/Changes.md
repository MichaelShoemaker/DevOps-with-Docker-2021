Changed Backend Dockerfile:

ENV REQUEST_ORIGIN=http://frontend:5000

to

ENV REQUEST_ORIGIN=http://localhost


Changed Frontend Dockerfile:

ENV REACT_APP_BACKEND_URL=http://backend:8080/

to

ENV REACT_APP_BACKEND_URL=http://localhost:8080/



Had to use docker-compose stop instead of docker-compose down to get the images rebuilt correctly.
