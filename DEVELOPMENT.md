## Local dev setup

- Install the recommended VSCode extensions. This includes `pylint` (Python linting) and `black` (Python formatting). VSCode is setup via the `settings.json` to format on save.

> [!Tip]
> I've specified recommended extensions, you can install them in VSCode by using [the "recommended" filter](https://code.visualstudio.com/docs/editor/extension-marketplace#_extensions-view-filter-and-commands).

- Install `SageMath` as described [here](https://github.com/matematiflo/CompAssistedMath2024/tree/main/Sage#installation-of-sage-via-conda-forge).

- Access the `sage` shell by typing `mamba activate sage` and then `sage` in your terminal. Then install the `pylint` package: `pip install pylint`. Otherwise, you won't be able to format/lint the Python code.
