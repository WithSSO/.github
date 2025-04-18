## Tax-free SSO
### What's this?
We provide sso.tax-free single sign-on implementations for open source projects.

[Github Link (github.com/withsso)](https://github.com/withsso)

### Why?
We completely agree with the reasoning on [sso.tax](https://sso.tax) - SSO is a baseline security feature that should not be restricted to a "Contact us for pricing" Enterprise tier.
In the cybersecurity landscape we're currently in, adding OpenID Connect as an SSO method to your app provides a set of baseline security features where the individual user can then connect their own IDP, and implement multi-factor authentication in hundreds of different ways, shapes or forms. 
In addition, SSO is often easier to implement than custom authentication.

### How do I make money with my app if not restricting features like SSO?
we completely understand the reasoning behind locking certain features to paid subscribers, developers have a right to earn money for their work. We just firmly believe that limiting (all) SSO is not the right way to go.

If you implement OpenID Connect on the free tier, here are a couple of alternative approaches that would still allow you to draw a line between home and business users:

- Limiting or disabling auto-provisioning for SSO (user accounts have to exist before being able to sign in, no auto-creation)
- Limiting a subset of OIDC features like automatic group memberships, permissions based on OIDC sessions
- Setting a user limit on the number of SSO users that are allowed to exist in the free tier
- Allowing SSO, but limiting LDAP and/or SAML2
- Setting a minor one-time or yearly **publicly available** fee or required sponsorship for the use of SSO

### What about limiting OIDC providers to Github and Microsoft?
If your target audience is the open source space, this is likely going to be a less than popular alternative. Many users have their own, local IDPs like Keycloak, Authelia, Authentik, Zitadel and others and would very much prefer to use one of those instead of a third party.

### How can we be sure your code is safe?
Everything happens in public. All code and container builds happen within Github actions, where the logs, checksums and information can be viewed by anyone using the application. 
Where required, we use OSSign (https://ossign.org) to sign the executables to make them runnable on Windows, Mac or other devices.

### I've added SSO to [oss project], can you help us with hosting and maintenance?
If the license for the project permits, yes. Open an issue in [this repository](https://github.com/withsso/.github) with the issue template "Project Request"

### Who are we?
We're a team of developers and self-hosters believing in a more secure open source space.
