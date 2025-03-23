# Pull Request Guide

This guide helps you get set up to contribute to Vedro’s **Python-based** repositories, such as the [core framework](https://github.com/vedro-universe/vedro) and [official Python plugins](https://github.com/search?q=topic%3Avedro-plugin+org%3Avedro-universe&type=Repositories). For other repositories, like [vedro-pycharm](https://github.com/vedro-universe/vedro-pycharm-plugin) (Java) or [vedro-vscode](https://github.com/vedro-universe/vedro-vscode) (TypeScript), different steps or technologies may apply.

Follow these instructions to fork the repo, run tests, and prepare your changes for a pull request.

## 1. Fork the Repository

1. Visit the repository you want to contribute to.
2. Click the «Fork» button at the top-right corner of the page.  

For more information on forking and submitting pull requests, see GitHub’s official guide: [Contributing to a project](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project).

## 2. Get to Know the Repo Structure

Most Python repositories for Vedro follow a similar layout:

- `vedro/` or `<plugin_name>/`  
    Contains the source code for the framework or plugin. For example, if the plugin is named [vedro-httpx](https://github.com/vedro-universe/vedro-httpx), the main source folder is also called `vedro_httpx`.
- `tests/`  
  Holds all automated tests for the project.
- `.github/`  
  Includes CI/CD pipeline configurations.  
- `Makefile`  
  Offers useful commands (e.g., installing dependencies, running tests, linting).

> **Tip**: Understanding this layout helps you find where to add or modify code, and where to place new tests.

## 3. Set Up Your Environment

Clone your fork locally and navigate to the project directory. Then create and activate a virtual environment. You can do this with:

```shell
$ python -m venv .venv
$ source .venv/bin/activate
```

This is the [standard way](https://docs.python.org/3/library/venv.html) to create a Python virtual environment. However, if you prefer other tools like pyenv or pipenv, feel free to use those instead.

## 4. Install Dependencies & Run Tests

To quickly install dependencies, check code quality, and run tests, you can use the Makefile:

```shell
$ make
```

This command:
- Installs required packages  
- Lints your code with `flake8`, checks type hints with `mypy`, etc.  
- Runs all tests in the `tests/` folder

For more details about these commands, see the [Makefile](https://github.com/vedro-universe/vedro/blob/main/Makefile) in the core Vedro repo. Other Python plugin repositories have a similar `Makefile`.

## 5. Develop Your Changes

Implement your fixes or features in the appropriate files. If you need to add new tests, place them in the `tests/` directory. After coding:

1. Run `make lint test` to ensure your changes pass code checks and tests.  
2. Commit and push your changes to your fork.

> **Tip**: To run Vedro scenarios locally with your new changes, use `vedro run` or `python -m vedro run`.

## 6. Open a Pull Request

Once your branch is ready, return to GitHub and open a Pull Request (PR) from your fork. Provide:

- A clear title that summarizes the change.  
- A description that includes a «Problem» section, explaining what issue the PR solves. See examples at [Vedro Issues](https://github.com/vedro-universe/vedro/issues?q=is%3Aissue).

If your pull request addresses a specific issue, reference it in your PR description using a [supported keyword](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword). This will automatically link and close the issue once the PR is merged.

We strongly encourage linking every pull request to an existing issue. If no corresponding issue exists, [create one first](https://github.com/vedro-universe/vedro/issues/new) so the community can discuss the proposed changes before you open your PR.

---

**That’s it!** Once your PR is merged, your contribution becomes part of Vedro’s codebase. Thank you for helping us improve and grow the framework, your efforts truly make a difference!

If you have any questions, please reach out on [X (Twitter)](https://x.com/vedro_universe), [Instagram](https://www.instagram.com/vedro_universe/), or join us on [Slack](https://slack.vedro.io).
