# Docker Configuration Assignment Report

## AWS Instance Access
AWS Instance Link: http://13.53.42.188/
#only http requests 

## Application Details
- **IP Address:** 172.18.0.2
- **MAC Address:** 00:00:00:00:00:00
- **Username:** Guest
- **Timestamp:** 2024-11-03 18:22:39

## Identified Issues and Resolution Steps
Several typographical errors were found and corrected during the setup process:

### Nginx Configuration Corrections:
- Base image update: Changed `FROM nginx:latests` to `FROM nginx:latest`
- Configuration file path correction: `COPY nginix.conf /etc/nginx/nginx.conf` to `COPY nginx.conf /etc/nginx/nginx.conf`
- Port exposure: Changed `EXPOSE "eighty"` to `EXPOSE 80`
- Command syntax update: Changed `CMD ["nginx", "-g", "daemon of;"]` to `CMD ["nginx", "-g", "daemon off;"]`
- Worker configuration corrections:
  - `worker_process` to `worker_processes`
  - `worker_connection` to `worker_connections`
- Include directive path correction: Changed from `include /etc/nginx/mime.typess` to `include /etc/nginx/mime.types`
- Configuration type correction: `default_typ` to `default_type`

### Python Application Corrections:
- Working directory path: Changed `WORKDIR /appp` to `WORKDIR /app`
- File copy command: Updated `COPY appy.py /app` to `COPY app.py /app`
- Package installation: Changed `RUN pip install flask netiface` to `RUN pip install flask netifaces`
- Port exposure: Updated `EXPOSE "eight thousand"` to `EXPOSE 8000`
- Command correction: Changed `CMD [ "pythn", "app.py" ]` to `CMD [ "python", "app.py" ]`

## Summary
The assignment focused on Docker container configuration for Nginx and Python applications. Multiple typographical errors were identified and corrected in configuration files and Dockerfiles. The major corrections included updating base images, command syntax, and port definitions. After implementing these corrections, the applications successfully ran in a containerized environment, resulting in improved functionality and enhanced performance.

## Status
Assignment completed successfully!
