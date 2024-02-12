Intent: to learn the micro service concepts
As of now in main branch of all the service started with ms_stream leverage the spring boot and spring cloud 3.1 version
Tech stack:
Spring boot - Spring Data JPA, Spring Security,Spring WEB,Logback ,JWT 
Spring cloud- Eureka ,Cloud Config
MySql
MINIO for object storage via Docker Images as below command
docker run -p 9000:9000 -d -p 9001:9001 -e "MINIO_ROOT_USER=minio99" -e "MINIO_ROOT_PASSWORD=minio123" quay.io/minio/minio server /data --console-address ":9001"

Below is the description of the Micro Services
ms_stream_dependencies_bom for common dependencies
ms_stream_util is common library which can be added as a dependency across the other micro service this is a non deployeable independent library
ms_stream_userService is a micro service which store the user record and also provide the register and login api which issues the JWT token
ms_stream_review is a micro service which contains the api to like/deslike the video and also post comment and reply to comment feature
ms_stream_videoService is a micro service which contains the API to upload and stream the video
ms_stream_service_registry is a micro service which stores the eureka service registry

![Diagram](https://shorturl.at/mvP34)
