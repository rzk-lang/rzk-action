# This is a sample literate Rzk Markdown file

```rzk
#lang rzk-1
```

Here's a sample definition to typecheck:

```rzk
#define modus-ponens
  ( A B : U)
  : ( A → B) → A → B
  := \ f x → f x
```
