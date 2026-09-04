# Required repository controls

Apply a ruleset to every active repository's default branch with these minimum controls:

- require a pull request and at least one approval;
- dismiss stale approvals after new commits;
- require review from Code Owners for security-sensitive paths;
- require all configured CI and integrity checks;
- require conversation resolution and a linear history;
- block force-pushes and branch deletion;
- restrict bypass to an audited emergency owner group;
- enable secret scanning, push protection, Dependabot alerts and private vulnerability reporting;
- preserve signed tags or release attestations for published artifacts.

The organization `.github` repository supplies policy defaults, but GitHub does not apply branch protection from a file. An organization administrator must configure and periodically audit these controls in repository rulesets.
