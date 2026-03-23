# Security Policy

**TechKnowMad Labs Private Limited** takes security seriously. This policy outlines our vulnerability disclosure process and security practices for all public repositories in the TECHKNOWMAD-LABS organization.

## Supported Versions

The following versions are currently supported with security updates:

| Version | Released | End of Support | Status |
|---------|----------|-----------------|---------|
| 2.x     | 2026-Q1  | 2027-Q1         | Active  |
| 1.x     | 2025-Q4  | 2026-Q3         | LTS     |
| 0.x     | Pre-2025 | 2025-12-31      | Deprecated |

Critical security patches are provided for Active and LTS versions. We recommend upgrading to the latest stable release promptly.

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.** Instead, please report security issues responsibly to our security team.

### How to Report

1. **Email**: Send a detailed report to `security@techknowmad.ai`
2. **Include**:
   - Description of the vulnerability
   - Steps to reproduce (if applicable)
   - Potential impact and severity assessment
   - Suggested fix (if available)
   - Your contact information for follow-up

3. **PGP Encryption** (Optional but recommended):
   - Encrypt your report using our PGP key:
   - **Fingerprint**: `TBD-SECURITY-KEY-PLACEHOLDER`
   - Key available at: https://github.com/TECHKNOWMAD-LABS/.github/security-key.asc

### Response Timeline

We commit to the following timelines for all reported vulnerabilities:

- **Acknowledgment**: Within 48 hours of receipt
- **Triage**: Within 5 business days (determine severity and scope)
- **Fix & Release**:
  - Critical vulnerabilities: 30 days
  - High vulnerabilities: 60 days
  - Medium vulnerabilities: 90 days
  - Low vulnerabilities: 120 days or next planned release

Fixes will be applied to all actively supported versions.

## Scope

### In Scope

Security issues in the following are eligible for coordinated disclosure:

- All public repositories in the TECHKNOWMAD-LABS GitHub organization
- Published API endpoints and interfaces
- Cryptographic implementations
- Authentication and authorization mechanisms
- Data validation and sanitization
- Dependency vulnerabilities affecting public code

### Out of Scope

The following are **not** in scope for this program:

- Social engineering, phishing, or physical security
- Denial of Service (DoS) attacks
- Attacks requiring private API keys, credentials, or internal system access
- Reports of outdated or unpatched third-party dependencies (without proof of active exploitation)
- Vulnerabilities in unsupported versions
- Missing security headers on non-critical endpoints
- Email forwarding configuration issues

## Safe Harbor

We appreciate responsible security researchers and commit to the following:

1. **No Legal Action**: We will not pursue civil, criminal, or regulatory action against individuals who:
   - Report vulnerabilities in good faith
   - Avoid unauthorized data access, service disruption, or privacy violations
   - Do not exploit vulnerabilities for financial gain
   - Respect our coordinated disclosure timeline

2. **Cooperation**: We will work with you transparently to understand and resolve the issue.

3. **Recognition**: All good-faith reports will be credited (if desired) in our Security Hall of Fame.

## Recognition

Individuals who responsibly disclose and report security vulnerabilities may be recognized in our **Security Hall of Fame**, published at:

https://github.com/TECHKNOWMAD-LABS/security-hall-of-fame

Recognition includes:
- Your name (or pseudonym) and affiliation
- Vulnerability description and CVE reference (if applicable)
- Date of disclosure

You may opt out of public recognition by requesting anonymity in your initial report.

## Disclosure Policy

### Coordinated Disclosure

We follow a coordinated disclosure model:

1. **Report Submission**: You submit the vulnerability to `security@techknowmad.ai`
2. **Acknowledgment & Triage**: We acknowledge receipt and assess severity within 5 business days
3. **Remediation**: We develop, test, and prepare a fix
4. **Embargoed Disclosure**: We coordinate with you on a disclosure date (typically within 90 days)
5. **Public Release**: We publish a security advisory and release fixed versions simultaneously
6. **Public Disclosure**: You may disclose the vulnerability publicly after our release

### Embargo Window

- **Default**: 90 days from vulnerability triage completion
- **Reduction**: May be shortened by mutual agreement if fix is delayed
- **Extension**: May be extended if remediation requires significant refactoring

### Post-Disclosure

Once fixed versions are publicly available:
- We publish a security advisory with CVE reference (if applicable)
- Details are added to our SECURITY.md changelog
- Security bulletin distributed to users

## Security Updates and Advisories

Security advisories are published at:
- GitHub Security Advisories: https://github.com/TECHKNOWMAD-LABS/security/advisories
- RSS Feed: Available through GitHub Watch → Security Alerts

## Contact

- **Security Issues**: `security@techknowmad.ai`
- **General Questions**: `admin@techknowmad.ai`
- **Organization**: TechKnowMad Labs Private Limited, Chennai, India
