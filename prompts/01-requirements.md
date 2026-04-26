# Prompt: Generate System Requirements for Pointrr

You are a senior systems architect and infrastructure engineer.

Your task is to generate a **complete, production-grade requirements document** for a service called **Pointrr**.

## Context

Pointrr is a service that:
- Allows users to map an IP address to a subdomain under `*.pointrr.dev`
- Automatically provisions DNS records via Cloudflare API
- Updates Nginx configuration dynamically on a server
- Uses a lightweight, script-driven architecture (Perl-based)

## Technical Constraints

- Backend scripting: **Perl**
- Web server: **Nginx**
- DNS provider: **Cloudflare API**
- Environment variables must be used for sensitive data (API keys, tokens)
- System is manually triggered (not event-driven or fully automated)

## Output Requirements

Produce a structured requirements document with:

### 1. Functional Requirements
- Domain assignment workflow
- IP validation and mapping
- DNS provisioning via Cloudflare
- Nginx config generation and reload
- Logging and traceability

### 2. Non-Functional Requirements
- Performance expectations
- Security considerations (API keys, abuse prevention)
- Reliability and rollback strategy
- Scalability limits and assumptions

### 3. System Architecture
- High-level diagram (text-based)
- Component responsibilities
- Data flow (request → DNS → Nginx)

### 4. External Integrations
- Cloudflare API (zones, DNS records)
- Server-level execution permissions

### 5. Configuration Management
- Environment variables
- File paths (e.g., `/etc/nginx/sites-enabled/`)
- Deployment assumptions

### 6. Risks & Constraints
- DNS propagation delays
- Misconfiguration risks
- Manual trigger limitations

## Tone

- Precise
- Technical
- No fluff
- No marketing language

Output only the final document.
