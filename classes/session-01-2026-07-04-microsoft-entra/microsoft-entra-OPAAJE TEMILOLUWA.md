# My Notes — [REPLACE WITH YOUR FULL NAME]


# My Notes — Microsoft Entra Identity & Access Security

---

## Key Concepts I Learned

- Microsoft Entra ID is the cloud directory service (tenant, users, groups, directory roles) that all access controls in this session are built on; the session's core purpose was granting and controlling resource access using four tools: Conditional Access, SSPR, PIM, and identity-aware apps
- Full authentication strength spectrum, ranked strongest to weakest:
  - **Passwordless**: Windows Hello for Business, Passkeys (FIDO2), FIDO2 security keys, Microsoft Authenticator (phone sign-in)
  - **Multifactor**: Authenticator app (push/TOTP), OATH hardware tokens, SMS/voice call (legacy), Temporary Access Pass
  - **Single factor**: password, security questions (SSPR-only), email (SSPR-only) — fallback use only, not primary authentication
- MFA matters because even if an attacker steals a username and password, they're still blocked without the second verification layer
- Conditional Access is Entra's policy engine, working as **Signals → Decision → Enforcement**:
  - Signals: user/group, application, device state, named location, sign-in/user risk
  - Decision: allow, block, require MFA, require compliant device, require auth strength
  - Enforcement: grant controls, session controls, continuous access evaluation, sign-in frequency
- Sign-in risk (likelihood a login attempt isn't genuinely the account owner) and insider risk (risky data-related activity from inside the environment) are distinct signals that can trigger stricter policy enforcement
- Named locations let policies require MFA specifically for sign-ins originating outside approved geographic/network zones
- Standing privilege (permanent admin role assignments) is the largest blast radius risk in most tenants if an account is compromised
- PIM (Privileged Identity Management) converts permanent access into time-bound, approved, audited activations — Just-in-Time access requiring MFA and written justification, lasting a set window (e.g. 8–24 hours) before expiring
- Role delegation should be scoped to the task — a User Administrator or Password Administrator can handle password resets or new account creation, rather than defaulting every request to a Global Administrator; elevated role requests go through PIM instead, keeping the process structured and auditable
- Conditional Access is always application-specific — most real-world misconfiguration and troubleshooting issues trace back to forgotten scope, not the underlying policy logic

---

## Lab / Hands-On Work
Followed the mentor's live demo building a Conditional Access policy that enforces MFA using if-then logic. Continued following along as the policy was refined with named locations, then watched it get troubleshot in real time using a live test user to confirm behavior.

**What happened / Result**
Watched the policy get configured, tested against an actual sign-in attempt, and adjusted based on the results — this confirmed how the signals, decisions, and enforcement controls behave once genuinely applied, not just in theory.

**Challenges I faced**
- Forgetting to fork the repository
- Forgetting to sync the forked repository
- Forgetting to provide justification text
---

## My Takeaways

The most valuable part of this session was seeing the full chain connect end to end: Entra ID establishes identity, MFA verifies it, Conditional Access decides how to act on that verified identity, and PIM extends the same least-privilege thinking from sign-ins to privileged roles themselves. The point about role delegation — that not every request needs a Global Administrator, and that routine tasks can be handled by scoped roles like User or Password Administrator — was a practical reminder that access should always match what's actually needed, not default to the highest level available.

---

## Questions I Still Have

- What is Just-in-Time (JIT) access, and how does PIM implement it?
- What's the difference between authentication and authorization?
- Why is single-factor authentication considered insecure, even with a strong password?
- Why is Microsoft Entra the foundation for everything relating to cloud security?

---

## Resources I Found Useful

- SC900
- SC300
- MICROSOFT ENTRA

---

*Submitted by: [OPAAJE TEMILOLUWA] · [tee_el]*
