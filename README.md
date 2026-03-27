README

Portainer Templates for Traefik-Based Docker Deployments

This repository provides reusable Portainer stack templates designed for Docker environments that use Traefik as the reverse proxy. The templates are intended for self-hosted deployments where applications are published through Traefik on a shared external Docker network, then exposed publicly through Cloudflare Tunnel or another upstream routing layer.

Purpose

The goal of this project is to simplify the deployment of new applications in Portainer by providing templates that already include:

- Traefik label patterns
- external proxy network support
- reusable hostname and domain variables
- common deployment structures for generic apps, static sites, database-backed apps, and ebook services

These templates are designed to reduce repetitive manual editing and establish a consistent deployment pattern across multiple applications.

Current Templates

This repository currently includes templates for:

- Generic App Behind Traefik
- Generic App Plus MariaDB Behind Traefik
- Static Site Behind Traefik
- Calibre Behind Traefik
- Calibre-Web Behind Traefik

Deployment Pattern

The templates assume the following environment:

- Docker and Docker Compose are installed
- Portainer is running and can load custom template libraries
- Traefik is already deployed and working
- An external Docker network named `proxy` already exists
- Public DNS or Tunnel routing will be added separately after stack deployment

These templates do not create DNS records, Cloudflare Tunnel public hostnames, or Cloudflare Access policies automatically. Those steps must still be completed separately.

Repository Structure

```text
portainer-templates/
└── portainer-templates.json
