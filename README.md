cat << 'EOF' > README.md
# Custom Nginx Web Server on Docker & AWS EC2

This project demonstrates containerizing a static web application using Docker and deploying it on an AWS EC2 Linux instance.

## Tools & Concepts Used
* **OS & Cloud:** Ubuntu/Amazon Linux on AWS EC2 (`ens5` networking, private IP routing)
* **Containerization:** Docker (`nginx:alpine` base image, custom `Dockerfile`)
* **Networking & Troubleshooting:** Port mapping (`8080:80`), socket verification (`ss -tulnp`), HTTP testing (`curl`), and container log inspection (`docker logs`)
* **Version Control:** Git & GitHub

## Quick Start
```bash
docker build -t my-web-app:v1 .
docker run -d --name web-server -p 8080:80 my-web-app:v1
curl http://127.0.0.1:8080
```
EOF

git add README.md
git commit -m "Add project documentation in README"
git push
