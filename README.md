<!-- pam:product-page:start -->
<div align="center">

# PAM Application Skeleton

**Start with production structure, not an empty directory.**

The canonical API starter with typed DTOs, thin controllers, services, repositories, resources, migrations, tests, and integer-backed domain enums.

[![Release](https://img.shields.io/github/v/release/push-in/pam-skeleton?style=flat-square&label=stable)](https://github.com/push-in/pam-skeleton/releases)
![PHP](https://img.shields.io/badge/PHP-8.5-777BB4?style=flat-square&logo=php&logoColor=white)
![License](https://img.shields.io/github/license/push-in/pam-skeleton?style=flat-square)

**[Documentation](https://push-in.github.io/pam-docs/getting-started/first-app/) · [Why this exists](#why-this-exists) · [What you can build](#what-you-can-build) · [Quick start](#quick-start) · [Issues](https://github.com/push-in/pam-skeleton/issues)**

</div>

---

## Why this exists

The canonical API starter with typed DTOs, thin controllers, services, repositories, resources, migrations, tests, and integer-backed domain enums.

| | |
| --- | --- |
| **Role** | Application starter |
| **Execution path** | PAM HTTP · Eloquent · PHP 8.5 |
| **This repository owns** | Generated project structure and first executable vertical slice |
| **Boundary** | A starting point, not a framework dependency or runtime distribution |

## What you can build

- Starting a structured JSON API
- Teaching the recommended PAM application architecture
- Proving database, validation, resource, and test workflows end to end

## Quick start

```bash
pam init my-app --template api
cd my-app
pam doctor --fix
pam dev
```

The **[PAM documentation](https://push-in.github.io/pam-docs/getting-started/first-app/)** covers prerequisites, production setup, and the complete workflow. PAM projects keep normal manifests and lockfiles; product features stay in the package that owns them.
<!-- pam:product-page:end -->

> This branch targets PAM API 2.0. Use the published `1.x` skeleton until the
> PAM API 2.0 prerelease is available on Packagist.

## License

The PAM skeleton is open source under the
[Apache License 2.0](LICENSE). Application files copied from this
skeleton and code emitted by PAM generators may be used, modified, sublicensed,
and distributed under terms of your choice, as stated in the Additional Use
Grant.
