# Pam application

```bash
pam composer install
pam dev index.php
```

The API starts at `http://127.0.0.1:3000`.

Run the in-memory application test inside Pam's Embed SAPI:

```bash
pam composer test
```

## License

The PAM skeleton is open source under the
[Apache License 2.0](LICENSE). Application files copied from this
skeleton and code emitted by PAM generators may be used, modified, sublicensed,
and distributed under terms of your choice, as stated in the Additional Use
Grant.

## Create an application

Do not clone this repository for normal application development. Let PAM create,
install, and validate a project from the version compatible with your runtime:

```bash
pam init my-api --template api
cd my-api
pam doctor
pam dev index.php
```

The generated application exposes:

- `GET /api/ping` as a health-sized JSON example;
- `GET /api/users/{id}` as a route-parameter example;
- security-header middleware;
- an in-memory PHPUnit application test; and
- normal Composer metadata, autoloading, scripts, and lockfile behavior.

## Development workflow

```bash
pam dev index.php                 # persistent server with hot reload
pam test                          # contextual project tests
pam composer test                 # explicit Composer test script
pam doctor                        # runtime and project diagnostics
pam info --json                   # machine-readable project discovery
```

Set `PAM_PORT` to change the default listener from `3000`. Keep secrets in the
environment or an application-owned secret manager; never commit a populated
`.env` file.

## Add capabilities

```bash
pam init realtime-api --template api --socket
pam composer require pushinbr/pam-psr-bridge
pam composer require --dev pushinbr/pam-testing
```

Use `pam packages` and `pam add <name>` for official Native ecosystem
capabilities. PAM performs dependency metadata lookup and a dry-run compatibility
preflight before changing the project.

## Production

```bash
pam release --check
pam package
```

Before release, replace the example routes, configure explicit listener limits,
exercise error and timeout paths, verify trusted proxies and TLS termination,
and test the packaged artifact in the target environment. The generated
application is a starting point, not an authorization or domain model.

See the [first application guide](https://push-in.github.io/pam-docs/getting-started/first-app/),
[HTTP documentation](https://push-in.github.io/pam-docs/runtime/http/), and
[production guide](https://push-in.github.io/pam-docs/runtime/production/).
