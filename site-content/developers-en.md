# For developers

The wiki is a graph of linked points. Git stores roots and the home page; the server stores accounts, user points, subscriptions and discussions.

- Static copy: run `python3 build.py` and publish `dist/`; it does not run a database.
- Connected wiki: the selected shared server handles login and user actions.
- Independent server: a separate backend and PostgreSQL, with its own registrations and influence.

[Installation by mode](https://node06.neocities.org/setup/en/) · [Engine source](https://github.com/wratixor/node06) · [Server setup](https://github.com/wratixor/node06/blob/main/backend/README.md)

For your own roots, use a public content repository with `node06-roots.json`. A connected source updates data rather than executing fork code. The administrator chooses the update policy for their own fork.

[Server deployment](md://core/devlog-server-en)

[Repository roots](md://core/devlog-git-en)

[In Russian](md://local/developers-ru) · [Logs](md://local/logs-en) · [Geno-Dice: Wiki](md://local/welcome-en)
