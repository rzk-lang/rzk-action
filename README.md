# rzk-action

GitHub Action to check formalisations using [`rzk` proof assistant](https://github.com/rzk-lang/rzk).

## Usage example

This step runs `rzk typecheck` in the project's root directory, relying on `rzk.yaml` to provide the project structure:

```yml
- name: Check all files
  uses: rzk-lang/rzk-action@v1
```

The following example runs `rzk typecheck` on all literate Rzk Markdown files in the `src/` directory, using `rzk` version 0.7.1:

```yml
- name: Check all files
  uses: rzk-lang/rzk-action@v1
  with:
    rzk-version: v0.7.1
    files: src/**/*.rzk.md
```

## Inputs

| Name               | Required | Description                                          | Type    | Default                       |
| ------------------ | :------: | ---------------------------------------------------- | ------- | ----------------------------- |
| `rzk-version`      |    No    | `rzk` version to use, ex. `latest` or `v0.5.3`       | string  | `latest`                      |
| `files`            |    No    | Files to process, ex. `lib/**/*.rzk src/**/*.rzk.md` | string  | Rely on local `rzk.yaml` file |
| `system-rzk`       |    No    | Use `rzk` executable provided by the system          | boolean | `false`                       |
| `typecheck`        |    No    | Typecheck the input files                            | boolean | `true`                        |
| `check-formatting` |    No    | Check that the input files are well-formatted        | boolean | `false`                       |

It only makes sense to turn off typechecking when checking the formatting.

## Outputs

| Name          | Description                     | Type   |
| ------------- | ------------------------------- | ------ |
| `rzk-version` | `rzk` version used, ex. `0.6.6` | string |
