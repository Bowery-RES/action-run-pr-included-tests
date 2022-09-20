# action-run-pr-included-tests
This GH Action is intended to encapsulate logic for running included in PR end-to-end tests, which were modified or newly created (written in [Cypress](https://docs.cypress.io/)) with [Currents dev](https://currents.dev/#faq) platform.

## Input description

| Script       | Description                                                                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| github_token | Access token                                                                                                                                  |
| url          | One of the four env urls we usually use for test runs: `dev`, `stage`, `prod` or `custom`. These options are predefined.                      |
| customUrl    | Url of custom env (PR deploy, dev/prod env). You need set `url` to `custom` in order to run tests against this url.                           |
| base_ref     | Target branch of Pull Request.                                                                                                                |
| head_ref     | Current branch of Pull Request.                                                                                                               |
| ref          | Commit to which we want to checkout and on what we want to run tests, param for [action/checkout](https://github.com/actions/checkout#usage). |
| secret_name  | Name of the secret in aws secret manager.                                                                                                     |