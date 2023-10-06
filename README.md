# rzk-action

GitHub Action to check formalisations using [`rzk` proof assistant](https://github.com/fizruk/rzk).

## Usage example

This step runs `rzk typecheck` on all literate Rzk Markdown files in the `src/` directory:

```yml
- name: Check all files
  uses: rzk-lang/rzk-action@v1
  with:
    rzk-version: latest
    files: src/**/*.rzk.md
```

## Inputs

| Name          | Required | Description                                          | Type   | Default                        |
| ------------- | :------: | ---------------------------------------------------- | ------ | ------------------------------ |
| `rzk-version` |    No    | `rzk` version to use, ex. `latest` or `v0.5.3`       | string | `latest`                       |
| `files`       |    No    | Files to process, ex. `lib/**/*.rzk src/**/*.rzk.md` | string | Rely on local `rzk.yaml` file  |
