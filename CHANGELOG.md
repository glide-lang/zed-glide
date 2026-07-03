# Changelog

## 0.4.2

- Highlight the `self` receiver/value as a builtin variable everywhere, so it
  no longer drifts between the parameter and variable colours across `&self`,
  `self.field`, and a bare `self`.


## 0.4.1

Aligned with the Glide 0.4.1 compiler.

- Bumped the tree-sitter grammar to the current commit (tuple syntax, and
  correct parsing of `fn new` / the contextual `new` keyword as an identifier
  in name position).
- Synced the bundled queries (`highlights.scm`, `indents.scm`, `outline.scm`)
  with the monorepo grammar — tuple-index `@property` and tuple-pattern
  `@variable` highlighting.
- The bundled LSP now classifies the contextual `new` keyword (and method
  names) as functions in semantic tokens, so `fn new` / `Vector::new()` no
  longer render as a control keyword or type.

## 0.3.2

Initial Zed extension: tree-sitter grammar + `glide-lsp` integration.
