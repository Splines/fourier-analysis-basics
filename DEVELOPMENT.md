## Local dev setup

### Linting with `pylint`

- Install the recommended VSCode extensions. This includes `pylint` (Python linting) and `black` (Python formatting). VSCode is setup via the `settings.json` to format on save.

> [!Tip]
> I've specified recommended extensions, you can install them in VSCode by using [the "recommended" filter](https://code.visualstudio.com/docs/editor/extension-marketplace#_extensions-view-filter-and-commands).

- Install `SageMath` as described [here](https://github.com/matematiflo/CompAssistedMath2024/tree/main/Sage#installation-of-sage-via-conda-forge).

- Access the `sage` shell by typing `mamba activate sage` and then `sage` in your terminal. Then install the `pylint` package: `pip install pylint`. Otherwise, you won't be able to format/lint the Python code.

- After that, reload the VSCode window and Pylint should be good to go even inside Jupyter notebooks. With the cursor positioned in a Jupyter notebook *code* cell (*not* inside a markdown cell), press `Ctrl + Alt + L` (or `Shift + Alt + F` if the first one is not working) to format/lint the code. If none of these shortcuts are working, open the command palette in VSCode (`Ctrl + Shift + P`) and type `Format Document` or `Format Cell`.
