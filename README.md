# devops-a2-004

[![CI](https://github.com/HuzaifaQ-1/devops-a2-004/actions/workflows/ci.yml/badge.svg)](https://github.com/HuzaifaQ-1/devops-a2-004/actions/workflows/ci.yml)

A simple personal portfolio page for **Huzaifa Qazi (Roll No. 004)**, built for
Assignment 2 of the *DevOps for Cloud Computing* lab course.

The page is plain HTML and CSS. It is packaged in a Docker image (served by
nginx) and built automatically by GitHub Actions on every push to `main`.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The portfolio page |
| `style.css` | Page styling (orange, red and black theme) |
| `Dockerfile` | Packages the page into an nginx image |
| `.github/workflows/ci.yml` | CI: checks the page, builds and pushes the image |

## Run it locally with Docker

```bash
docker build -t huzaifa1001/devops-a2:manual .
docker run -d -p 8080:80 --name page huzaifa1001/devops-a2:manual
```

Then open <http://localhost:8080>.

## Docker Hub

Image: [`huzaifa1001/devops-a2`](https://hub.docker.com/r/huzaifa1001/devops-a2)
