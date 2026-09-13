# repo-doctor
# repo-doctor

A lightweight CLI that diagnoses the health of any public GitHub repository.

## Why?

Maintainers and contributors often lack a quick overview of a project's
health before investing time in it. `repo-doctor` gives you a one-command
snapshot: activity, responsiveness, license, CI, and bus factor signals.

## Install

```bash
pip install repo-doctor
```

## Usage

```bash
repo-doctor https://github.com/pallets/flask
# or
repo-doctor pallets/flask
```

Set a `GITHUB_TOKEN` environment variable to raise the API rate limit
from 60 to 5,000 requests/hour.

## Example output

```javascript
Repository: pallets/flask
Stars: 67,000 | Forks: 16,200 | Open issues: 121
Last push: 2026-09-10 (3 days ago)
License: BSD-3-Clause
CI workflow: found
Median issue response time: 2.1 days
Health score: 78/100
```

## Health score

The score (0-100) combines:

| Signal | Weight |
| --- | --- |
| Recent activity | 25 |
| Issue responsiveness | 25 |
| License present | 20 |
| CI configured | 15 |
| Multiple active committers | 15 |

## Contributing

Issues and pull requests are welcome. Please open an issue before
large changes. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT — see [LICENSE](LICENSE).
