# Security Test Plan

## Scope

- Repository hygiene for a profile/documentation-only repository
- Prevention of committed secrets or unsafe environment files
- Documentation traceability for AppSec expectations

## Risks Covered

- OWASP Top 10 2025 baseline applied only to the risks that make sense for a content repository: security misconfiguration and sensitive data exposure
- Lightweight ASVS/WSTG reference for secure repository handling

## Approach

- Run a deterministic Node-based hygiene check on every push/PR
- Document non-applicable items explicitly instead of inventing app-layer coverage

## Automated Scenarios

- Block committed `.env` files
- Detect common secret patterns such as private keys and access tokens

## Recommended Manual Scenarios

- Review profile links and badges periodically
- Add platform-level dependency and secret scanning if the repo grows beyond documentation

## Limitations And Assumptions

- This repository does not contain a web app, API or mobile project, so auth, session, authorization, headers, CORS, IDOR/BOLA, injection and upload scenarios are not applicable here
