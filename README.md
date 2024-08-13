This repository showcases two issues I have with devenv's composition feature.

This repository contains a top-level devenv project that imports the devenv `subproject`. `subproject` is a python/poetry project with `dbt` as a dependency.

The two issues I have are:
- In the top-level project, I receive the message "No pyproject.toml found. Run 'poetry init' to create one." because devenv seems to start poetry in the top-level project.
- I cannot use `dbt` in the top-level project.

The behavior I expect from reading https://devenv.sh/composing-using-imports/ is that I can use `dbt` in the top-level project because it is defined in `subproject`, and I do not expect devenv to start Poetry in the top-level project.
