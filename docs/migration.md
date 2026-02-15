# Migration Guide

## From monorepo path-based usage

Old:

```yaml
uses: LN-Zap/devenv-actions/.github/actions/setup-devenv@master
```

New:

```yaml
uses: LN-Zap/setup-devenv@v1
```

Old:

```yaml
uses: LN-Zap/devenv-actions/.github/actions/bake-devenv-image@master
```

New:

```yaml
uses: LN-Zap/bake-devenv-image@v1
```

## Benefits

- Cleaner consumer syntax
- Independent versioning/release cadence
- Better discoverability for each action
