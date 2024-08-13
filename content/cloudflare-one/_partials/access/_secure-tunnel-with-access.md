---
_build:
  publishResources: false
  render: never
  list: never
---

To secure your origin, you must validate the [application token](/cloudflare-one/identity/authorization-cookie/) issued by Cloudflare Access. Token validation ensures that any requests which bypass Cloudflare Access (for example, due to a network misconfiguration) are rejected.

One option is to configure the Cloudflare Tunnel daemon, `cloudflared`, to validate the token on your behalf. This is done by enabling [**Protect with Access**](/cloudflare-one/connections/connect-networks/configure-tunnels/origin-configuration/#access) in your Cloudflare Tunnel settings. Alternatively, if you do not wish to perform automatic validation with Cloudflare Tunnel, you can instead [manually configure your origin](/cloudflare-one/identity/authorization-cookie/validating-json/) to check all requests for a valid token.