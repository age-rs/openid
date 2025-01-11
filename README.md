# OpenID Connect & Discovery client library using async / await

## Legal

Dual-licensed under `MIT` or the [UNLICENSE](http://unlicense.org/).

## Features

Implements [OpenID Connect Core 1.0](https://openid.net/specs/openid-connect-core-1_0.html) and [OpenID Connect Discovery 1.0](https://openid.net/specs/openid-connect-discovery-1_0.html).

Implements [UMA2](https://docs.kantarainitiative.org/uma/wg/oauth-uma-federated-authz-2.0-09.html) - User Managed Access, an extension to OIDC/OAuth2. Use feature flag `uma2` to enable this feature.

Implements [OAuth 2.0 Token Introspection](https://datatracker.ietf.org/doc/html/rfc7662).

It supports Microsoft OIDC with feature `microsoft`. This adds methods for authentication and token validation, those skip issuer check.

Originally developed as a quick adaptation to leverage async/await functionality, based on [inth-oauth2](https://crates.io/crates/inth-oauth2) and [oidc](https://crates.io/crates/oidc), the library has since evolved into a mature and robust solution, offering expanded features and improved performance.

Using [reqwest](https://crates.io/crates/reqwest) for the HTTP client and [biscuit](https://crates.io/crates/biscuit) for Javascript Object Signing and Encryption (JOSE).

## Support:

You can contribute to the ongoing development and maintenance of OpenID library in various ways:

### Sponsorship

Your support, no matter how big or small, helps sustain the project and ensures its continued improvement. Reach out to explore sponsorship opportunities.

### Feedback

Whether you are a developer, user, or enthusiast, your feedback is invaluable. Share your thoughts, suggestions, and ideas to help shape the future of the library.

### Contribution

If you're passionate about open-source and have skills to share, consider contributing to the project. Every contribution counts!

Thank you for being part of OpenID community. Together, we are making authentication processes more accessible, reliable, and efficient for everyone.

## Usage

Add dependency to Cargo.toml:

```toml
[dependencies]
openid = "0.16"
```

By default we use native tls, if you want to use `rustls`:

```toml
[dependencies]
openid = { version = "0.16", default-features = false, features = ["rustls"] }
```

### Use case: [Warp](https://crates.io/crates/warp) web server with [JHipster](https://www.jhipster.tech/) generated frontend and [Google OpenID Connect](https://developers.google.com/identity/protocols/OpenIDConnect)

This example provides only Rust part, assuming just default JHipster frontend settings.

in Cargo.toml:

```toml
404: Not Found
```

in src/main.rs:

```rust, compile_fail
404: Not Found
```

See full example: [openid-examples: warp](https://github.com/kilork/openid-examples/blob/v0.16/examples/warp.rs)
