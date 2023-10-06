# rzk-action

GitHub Action to check formalisations using [`rzk` proof assistant](https://github.com/rzk-lang/rzk).

## Usage example

This step runs `rzk typecheck` in the project's root directory, relying on `rzk.yaml` to provide the project structure:

```yml
- name: Check all files
  uses: rzk-lang/rzk-action@v1
```

The following example runs `rzk typecheck` on all literate Rzk Markdown files in the `src/` directory, using `rzk` version 0.6.6:

```yml
- name: Check all files
  uses: rzk-lang/rzk-action@v1
  with:
    rzk-version: 0.6.6
    files: src/**/*.rzk.md
```

## Inputs

| Name          | Required | Description                                          | Type   | Default                       |
| ------------- | :------: | ---------------------------------------------------- | ------ | ----------------------------- |
| `rzk-version` |    No    | `rzk` version to use, ex. `latest` or `v0.5.3`       | string | `latest`                      |
| `files`       |    No    | Files to process, ex. `lib/**/*.rzk src/**/*.rzk.md` | string | Rely on local `rzk.yaml` file |
