# Branch Naming Convention (Template for Branch Names)

To keep the history organized, we standardize and organize the branches of our repository using the following format.

## Base Structure

`[type]/[issue-number]-[short-description-in-english]`

_Example: `feat/15-menu-interactive` or `fix/8-bot-crash`_

## Supported Branch Types:

1. **feat**: For the development of new significant features or functionalities.
   - _Example: `feat/42-payment-gateway-integration`_
2. **fix**: For the solution of errors, bugs, crashes of the application.
   - _Example: `fix/11-resolve-undefined-message-error`_
3. **hotfix**: For critical and very urgent solutions that have to go directly to production.
   - _Example: `hotfix/fix-production-downtime`_
4. **docs**: For the creation of documentation or textual modifications.
   - _Example: `docs/5-update-readme-instructions`_
5. **refactor**: For restructuring code, where functionalities do not vary and no new _features_ are added.
   - _Example: `refactor/22-extract-state-machine-logic`_
6. **chore**: Updates of npm packages, system scripts or general maintenance without change in direct code.
   - _Example: `chore/update-whatsapp-library`_

**Attention:** Try to make short descriptions without using spaces. Use hyphens (`-`) instead.
