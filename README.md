# Devenv Actions Hub

Documentation and examples hub for related Devenv GitHub Actions.

> Source code for actions lives in dedicated repositories. This repo intentionally contains no action implementation code.

## Action Repositories

| Action | Description |
| --- | --- |
| [bake-devenv-image](https://github.com/LN-Zap/bake-devenv-image) | Build-time generation of Devenv activation assets for runner images. |
| [setup-devenv](https://github.com/LN-Zap/setup-devenv) | Runtime Devenv activation and verification for workflow jobs. |

## Recommended composition

### 1) Setup-only workflow

```yaml
- uses: LN-Zap/setup-devenv
  with:
    mode: auto
```

### 2) Image bake workflow

```yaml
- uses: LN-Zap/setup-devenv
  with:
    mode: install

- uses: LN-Zap/bake-devenv-image
  with:
    snapshot_name: my-repo-devenv
```
