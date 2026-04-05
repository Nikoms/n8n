---
title: "SEVEN things about API security By Philippe De Ryck (en)"
date: 2026-04-05T11:28:27.034+02:00
category: videos
tags: [API security, OWASP, authorization, role-based access control, object-level authorization, sensitive data exposure, password reset security, brute force attack, username enumeration, JSON Web Tokens, server side request forgery, SSRF, internal security, perimeter security]
excerpt: "An in-depth session on API security covering authorization pitfalls, sensitive data exposure, brute force vulnerabilities in password resets, and server side request forgery, with practical recommendations and a live demo."
---

![thumbnail](https://i.ytimg.com/vi/xFzaFo0MiH8/maxresdefault.jpg?sqp=-oaymwEmCIAKENAF8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGH8gLSg0MA8=&rs=AOn4CLDOrQImNyzomAeNLfgy7_eiSw79UA)
[https://youtu.be/xFzaFo0MiH8?is=1co615DUATbo0LZ-](https://youtu.be/xFzaFo0MiH8?is=1co615DUATbo0LZ-)

## My thoughts

Not specified (yet)

## TLDR;
- APIs are everywhere and securing them is hard, with authorization vulnerabilities being a major issue.
- Authorization failures often lead to data theft or unauthorized actions; role explosion complicates authorization management.
- Function level authorization is common but object level authorization is often missing, leading to severe vulnerabilities.
- Centralizing authorization logic in a policy engine improves manageability, auditability, and security.
- Sensitive data exposure occurs when APIs leak unnecessary data, often due to returning full models instead of tailored DTOs.
- Username enumeration and brute force attacks on password reset functions are common and easy to carry out without proper protections.
- Using signed tokens (e.g., JWT) for sensitive codes prevents tampering and enhances security.
- Modern application borders are easy to breach; server-side request forgery (SSRF) exploits internal trust.
- SSRF is hard to prevent due to URL parsing ambiguities; best mitigations include hardcoding URLs and input normalization.
- Key takeaways: authorization policies must be auditable; APIs must be analyzed for data leaks and brute force vulnerabilities; internal systems require robust security beyond perimeter defenses.



## Content

### Introduction to API Security Challenges

In this session, the presenter emphasized the explosive growth of APIs and the increasing prevalence of security vulnerabilities in them. Despite the widespread adoption of APIs, securing them remains a challenging task often underestimated by developers and organizations. The talk references the OWASP API Security Top 10, a popular community-driven list updated recently, outlining the most common and dangerous API security issues.

> "APIs are everywhere these days and it turns out that API security issues are almost everywhere these days. Securing these APIs is hard."

### Authorization: The Hardest Part of API Security

Authorization was highlighted as a significant challenge—three out of ten API security issues relate directly to it. The issue is often that unauthorized users gain access to data or functions they shouldn't, which can cascade into severe breaches.

The presenter explained common pitfalls such as missing authorization checks (e.g., no control on adding family members in a smart scale app), leading to unauthorized actions. He explained the concept of "Role Explosion" – as applications grow, many roles proliferate, causing complexity and poor maintainability in access control systems.

An effective solution is shifting from role-based access control (RBAC) that checks roles at endpoints, to permission-based access control where permissions are explicitly checked, decoupling roles from API endpoints. Furthermore, the complexity in object-level authorization (validating access to individual objects such as family records) is commonly overlooked, leading to the most critical issues in APIs.

Centralizing authorization logic into a dedicated policy engine, either custom or using solutions like Open Policy Agent, was recommended to ensure clarity, auditability, and better security management.

> "You have to really look at centralizing this authorization logic... having it spread out through your API routes is a recipe for failure."

### Sensitive Data Exposure and Best Practices

Another frequent vulnerability is sensitive data exposure, caused primarily by APIs returning whole model objects instead of tailored data transfer objects (DTOs). This results in leaking sensitive attributes such as user addresses or tokens that are never meant to be exposed.

The recommended approach is to apply a "deny by default" principle—only allow explicitly needed fields to be returned. Using DTOs or schema-based response views helps enforce this principle.

This issue manifests in many real-world cases, including password reset flows leaking reset tokens.

### Demonstration of Attacks: Username Enumeration and Password Reset Bruteforce

A live demo illustrated how simple it is to enumerate valid usernames using timing differences in responses due to password hash verifications (bcrypt). Attackers exploiting these timing differences can confirm which accounts exist.

The speaker demonstrated a brute-force attack against a password reset PIN code, showing how weak numeric codes (4 or 6 digits) are easily enumerated using penetration testing tools like Burp Suite. This leads to full account takeover.

Best mitigations include:
- Using consistent error messages to avoid username enumeration.
- Implementing rate limiting to prevent brute force attempts.
- Replacing guessable codes with signed, tamper-proof tokens such as JSON Web Tokens (JWT).

> "You can no longer change a single bit of that value and that makes things better."

### Internal Perimeter and Server Side Request Forgery (SSRF)

The session also covered the misconception of trust inside network perimeters. Attackers increasingly exploit legitimate internal functionalities to reach sensitive systems.

SSRF vulnerabilities occur when an API endpoint accepts a URL from a user and the backend server fetches data from that URL without sufficient validation. Attackers can trick the server into querying internal systems.

Challenges include ambiguity in URL parsing across different libraries, such as the "double @ sign" trick that can fool different parsers to send requests to unintended hosts.

Practical mitigations include:
- Hardcoding or restricting hosts that the server will request.
- Normalizing and reparsing the URL in a centralized manner before validation and use to avoid parser discrepancies.

### Key Takeaways

1. Authorization policies must be simple, understandable, and auditable. Centralizing policy decision logic is crucial.
2. Avoid sensitive data leakage by carefully shaping API responses and adopting deny-by-default models.
3. Be vigilant about brute-force and enumeration attacks: implement uniform responses and rate limiting.
4. Do not rely solely on perimeter security: internal systems require equal protection to external-facing APIs.

> "Perimeter is easy to breach in a variety of ways; internal systems need to be protected just as much as outside systems."

This comprehensive overview into API security reveals how seemingly simple API features can hide significant vulnerabilities and how thoughtful design patterns and security practices are essential for protecting modern applications.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/925](https://github.com/Nikoms/n8n/tree/main/ongoing/925)