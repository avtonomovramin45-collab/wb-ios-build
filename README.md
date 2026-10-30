# wb-ios-build (temporary)

Unsigned build of the iOS proxy app from
[kulikov0/whitelist-bypass](https://github.com/kulikov0/whitelist-bypass) **v0.4.4**
(MIT, see LICENSE) with two small fixes so the Telemost joiner can use Yandex's
TURN servers over TCP when UDP is blocked:

- `patches/tcp-turn-v044.patch` — enable TCP4 ICE network type in the Telemost joiner;
- `patches/headless-client-v010-tcpturn.patch` — relay candidates obtained via
  TURN/TCP are UDP (relayed address), not tcp4, so they pair with the SFU's
  UDP candidates.

Built on GitHub Actions (macOS), installed via SideStore. This repository is
temporary and will be deleted after the build.
