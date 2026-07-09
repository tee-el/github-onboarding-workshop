# My Notes — Berna Namulyowa

## Key Concepts I Learned

<!-- Write the main ideas covered in today's session -->
Secure Access to Resources by Using Microsoft Entra
I learned that this is a practical defense-in-depth approach used to authenticate, allow privileged access, and support identity-aware AI applications.
Passwordless is the strongest authentication method, and this includes Windows Hello for Business, Passkeys, FIDO2 security keys, and Microsoft Authenticator.
You can also add conditional access policies to either a group or a user.
Using Just-in-Time privileged access eliminates standing permissions.


Authenticate Your API Plugin for Declarative Agents with Secured APIs
Declarative agents for Microsoft 365 Copilot can be used to create AI-powered assistants that you can customize by giving them instructions to do anything you want them to do.


Integrate an API Plugin with an API Secured with a Key
---

## Lab / Hands-On Work

<!-- Describe what you did in the lab. Include steps, commands, or screenshots descriptions -->
Lab 1: Deploy MFA with Conditional Access
Steps:
Use the Microsoft Entra Portal.
Configure a Named Location using either trusted IP boundaries or a country. In my case, I used IP boundaries.
Add a policy to Conditional Access.
Under the added policy, attach it to a specific user.
Set the policy to report-only and review the sign-in logs.


Lab 2: Onboard a Role into PIM
Steps:
Under Entra ID, select PIM, then Roles.
Select User Administrator and set the activation max duration to your preference.
Add assignments for the target administrators — don't forget to remove their active permanent assignments.
Configure the activation approval.
Activate the role for a user and confirm the MFA, approval flow, and audit-log entries.
Schedule a quarterly access review on the role.
  
### What I did
I completed Lab 1:
Used the Microsoft Entra Portal.
Configured a Named Location using trusted IP boundaries (192.168.137.1/24).
Added a policy to Conditional Access.
Attached the policy to a specific user.
Set the policy to report-only and reviewed the sign-in logs.

### What happened / Result
I used another browser, and when the user was prompted to sign in, an authenticator request popped up, requiring them to install the Authenticator app.

### Challenges I faced
Lab 2 is still challenging me but i will do it.

---

## My Takeaways

<!-- What was most valuable to you personally from this session? -->
The practical part, mostly Lab 1, was a success on the first attempt.

I also valued the knowledge gained on securing API plugins using declarative agents.
---

## Questions I Still Have

<!-- Anything you want to follow up on or ask the mentor -->

-
-

---

## Resources I Found Useful

<!-- Any links, docs, or Microsoft Learn modules you found helpful -->
https://learn.microsoft.com/en-us/training/modules/copilot-declarative-agent-api-plugin-auth/7-summary
-

---

*Submitted by: Berna Namulyowa · nbernah*
