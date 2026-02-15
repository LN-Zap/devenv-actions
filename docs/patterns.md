# Usage Patterns

## Fast setup path (custom image runner)

1. Build/update image using `setup-devenv` (install mode) + `bake-devenv-image`
2. Use `setup-devenv` in `image` or `auto` mode in fast-path workflows

## Portable fallback path

Use `setup-devenv` in `auto` mode to fallback to dynamic activation when image assets are missing.

## Validation checks

In consumer workflows, verify:
- required files (e.g. `rulesync.jsonc`)
- command availability (`devenv`, `node`, `python3`, `jq`)

## Pinning strategy

- Initial rollout: pin to SHA
- Stable stage: pin to `@v1`
