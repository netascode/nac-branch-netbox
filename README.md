Provisions Network as Code for the Unified Branch, pulling IP addressing (prefixes and gateway addresses) from NetBox.

This is the repo associated with the lab https://selfservelabs.cisco.com/schedule/unified-branch-network-as-code

How the reservation works: https://app.vidcast.io/share/f4cc0a91-ef7b-48c0-8c33-e9ff81fe1f83

## CI configuration

Workflows run under the `unified-branch-network-as-code` GitHub Environment. Configure it with:

**Variables** (`vars.*`): `NETBOX_URL`, `ORG_NAME`, `BRANCH1_MX_SERIAL`, `BRANCH1_MS_SERIAL`, `BRANCH1_CW_SERIAL`, `BRANCH2_MX_SERIAL`, `BRANCH2_MS_SERIAL`, `BRANCH2_CW_SERIAL`.

**Secrets** (`secrets.*`): `MERAKI_API_KEY`, `NETBOX_TOKEN`.

> NetBox Cloud tokens look like `nbt_<key-id>.<secret>` — store the **full string**, not just the part after the dot, or API calls will fail with `Invalid v1 token`.

The remaining values still read from a local, gitignored `.env` (see `.env.example`) aren't yet available in CI and need the same migration.
