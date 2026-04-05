# Build commands:
#   Default (index.html) : docker build -t my-app .
#   Use index1.html      : docker build --build-arg INDEX_FILE=index1.html -t my-app .
#
# Run command:
#   docker run -p 8080:8080 my-app

FROM nginx

RUN apt-get update && apt-get upgrade -y

ARG INDEX_FILE=index.html

COPY index.html /usr/share/nginx/html/index.html
COPY index1.html /usr/share/nginx/html/index1.html

RUN cp /usr/share/nginx/html/${INDEX_FILE} /usr/share/nginx/html/index.html

EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
