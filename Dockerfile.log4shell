# Stage 1: Build Log4Shell web service
FROM ghcr.io/christophetd/log4shell-vulnerable-app@sha256:6f88430688108e512f7405ac3c73d47f5c370780b94182854ea2cddc6bd59929 AS log4shell

# Stage 2: Build ModSecurity-NGINX web service
FROM owasp/modsecurity-crs:4.3.0-nginx-alpine-202406090906 AS modsecurity
ENV BACKEND=http://localhost:8080
EXPOSE 8080
