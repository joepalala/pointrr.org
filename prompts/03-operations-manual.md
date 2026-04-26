# Prompt: Create Operations Manual for Pointrr (Manual Processes)

You are a senior DevOps engineer and operations lead.

Your task is to create a **clear, no-nonsense operations manual** for running the Pointrr service.

## Context

- Pointrr is **not automated**
- All actions are manually triggered by an operator
- System includes:
  - Perl scripts (DNS + Nginx config)
  - Cloudflare API calls
  - Nginx reloads
  - Optional PHP email notification

## Objective

Produce a **step-by-step operational playbook** that a competent engineer can follow without ambiguity.

---

## Required Sections

### 1. Overview
- What the operator is responsible for
- System boundaries

### 2. Prerequisites
- Server access (SSH)
- Required environment variables
- API keys (Cloudflare)
- File permissions

### 3. Standard Workflow: Register New Subdomain

Step-by-step:

1. Validate request (IP + subdomain)
2. Run Perl script to:
   - Call Cloudflare API
   - Create DNS record
3. Generate Nginx config
4. Test Nginx config (`nginx -t`)
5. Reload Nginx
6. (Optional) Trigger PHP email notification

### 4. Verification

- DNS resolution check (`dig`, `nslookup`)
- HTTP response check
- Nginx config presence

### 5. Rollback Procedure

- Remove DNS record via API
- Delete Nginx config
- Reload Nginx
- Confirm cleanup

### 6. Troubleshooting

- Common failure points:
  - API failure
  - Nginx syntax errors
  - DNS not propagating
- Exact commands to debug

### 7. Logging

- Where logs are stored
- What to check:
  - Nginx logs
  - Script output logs

### 8. Security Practices

- Protect API keys
- Limit script execution permissions
- Avoid arbitrary input execution

---

## Style Guidelines

- Command-first writing (imperative tone)
- No theory, only actionable steps
- Include real command examples where useful
- Assume reader is technical but unfamiliar with system

Output only the final manual.
