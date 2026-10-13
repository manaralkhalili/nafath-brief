Version: NAFATH-V1
Your track: Data

## Overview
A secure national digital login service integrates software, AI, mobile, networking, cybersecurity, and data management into a cohesive system. OAuth 2.0 and OpenID Connect manage user identity authentication and resource access, while mobile apps rely on Android runtime permissions to protect sensitive device sensors. High-speed networking with DNS over HTTPS encrypts query traffic to prevent eavesdropping, while cybersecurity controls ensure phishing-resistant multi-factor authentication. AI models analyze authentication logs in real time to flag anomaly patterns, and robust data governance protects citizens' personal identifiable information under national privacy laws. As part of this comprehensive architecture, this brief focuses on data protection obligations under Oman's Personal Data Protection Law.
## Software
OAuth 2.0 and OpenID Connect (OIDC) serve distinct identity functions in modern web architectures. OAuth 2.0 is an authorization framework that enables applications to obtain limited access to user resources on an HTTP service without exposing user credentials. In contrast, OpenID Connect is an authentication layer built directly on top of OAuth 2.0 that verifies the end-user's identity and provides profile information in an ID token. OpenID Connect is designed for user login, while OAuth 2.0 is designed for delegated resource access.

Resource: RFC 6749 - The OAuth 2.0 Authorization Framework - https://datatracker.ietf.org/doc/html/rfc6749 
## AI
Deploying an automated AI risk model for suspicious login detection requires proactive governance to prevent operational vulnerabilities. Under the NIST AI Risk Management Framework (AI RMF 1.0), key risks must be managed before live deployment, including statistical bias leading to false positive account locks, lack of explainability in automated decisions, and susceptibility to adversarial attacks or data drift over time. Ensuring system trustworthiness requires rigorous validation of accuracy, security, privacy protection, and transparent human oversight.

Resource: NIST AI Risk Management Framework (AI RMF 1.0) - https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf
## Mobile
Android's runtime permission model restricts application access to sensitive device capabilities, system resources, and user data, such as location, camera, and contact records. The login app cannot access dangerous resources by default. Instead, it must prompt the user for permission explicitly at runtime when the specific feature is first requested in context. Normal permissions, such as basic network access, are granted automatically upon installation without explicit runtime prompts.

Resource: Android Developers - Permissions on Android - https://developer.android.com/guide/topics/permissions/overview
## Networking
DNS over HTTPS (DoH) is a protocol designed to perform remote Domain Name System (DNS) resolution via the HTTPS protocol. By encapsulating DNS queries and responses within encrypted TLS traffic, DoH protects users of the service from local eavesdropping, Man-in-the-Middle (MitM) tracking, and packet inspection by third-party network operators. However, DoH does not protect users from malicious server endpoints, upstream DNS resolver logging, or underlying IP address exposure at the transport layer.

Resource: RFC 8484 - DNS Queries over HTTPS (DoH) - https://datatracker.ietf.org/doc/html/rfc8484
## Cybersecurity
An authentication method is considered "phishing-resistant" when it cryptographically binds the authentication session to a specific origin service and relies on secure channels that cannot be bypassed or replicated by malicious third-party relay sites. Hardware-based FIDO2 / WebAuthn security keys and platform authenticators (such as Windows Hello or Apple Touch ID using public-key cryptography) qualify as phishing-resistant. Conversely, traditional multi-factor authentication methods like SMS OTP, email OTP, and push notifications without origin binding do not qualify because they remain vulnerable to interception and real-time adversary-in-the-middle phishing portals.

Resource: NIST Special Publication 800-63B - Digital Identity Guidelines: Authentication and Lifecycle Management - https://pages.nist.gov/800-63-3/sp800-63b.html
## Data
Under Oman's Personal Data Protection Law (Promulgated by Royal Decree No. 6/2022), the authority acting as a data controller must obtain explicit, informed, and documented consent from citizens prior to collecting, processing, or storing personal data. The authority is legally obligated to implement strict technical and organizational measures to safeguard personal data against unauthorized access, leakage, or alteration, ensure data accuracy, retain data only as long as necessary for the specified purpose, and respect individuals' rights to access and correct their personal information.

Resource: Ministry of Transport, Communications and Information Technology - Personal Data Protection Law - https://www.mtcit.gov.om/ITAPortal/DocumentLibrary/UserFiles/Files/PersonalDataProtectionLawEN.pdf
## Misconception in My Track
A common misconception regarding data protection in Oman is that obtaining initial consent from citizens permits an authority to store, process, and repurpose personal data indefinitely for any future internal projects. In reality, under Oman's Personal Data Protection Law, consent must be specific and for a defined purpose, and data must not be kept longer than necessary to fulfill that original purpose. Furthermore, data subjects retain the legal right to withdraw their consent at any time. This principle is explicitly established in Chapter Three regarding the provisions of processing personal data and data subjects' rights under the Personal Data Protection Law.
## Open Question
What specific cross-border data transfer mechanisms and localized cloud storage requirements does Oman's Personal Data Protection Law mandate when integrating external cloud identity providers?

  
