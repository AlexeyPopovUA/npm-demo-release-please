# npm-demo-release-please

[![NPM Package](https://img.shields.io/npm/v/npm-demo-release-please)](https://www.npmjs.com/package/npm-demo-release-please)

Demo library showcasing **Release Please** automation for NPM package publishing.

## Features

- ✅ PR-based release workflow using Google's Release Please
- ✅ Automatic changelog generation from conventional commits
- ✅ GitHub native integration with manifest-based configuration  
- ✅ Feature branch publishing with custom NPM dist-tags
- ✅ Automatic cleanup of feature branch aliases

## Usage

```javascript
import { hello } from 'npm-demo-release-please';

console.log(hello('World')); // "Hello, World!"
```

## Release Workflow

### Main Branch
1. Commits are made using conventional commit messages
2. Release Please analyzes commits and creates a release PR
3. When the release PR is merged, a new version is automatically published

### Feature Branches
Pushes to `feature/**` or `feat/**` branches publish pre-release versions with branch-specific NPM tags.

## Commit Message Format

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New features (minor version bump)
- `fix:` - Bug fixes (patch version bump)
- `feat!:` or `BREAKING CHANGE:` - Breaking changes (major version bump)

## Example Scenarios

1. **Feature Release**: `feat: add new greeting function`
2. **Bug Fix**: `fix: handle empty name parameter`
3. **Breaking Change**: `feat!: change function signature`
4. **Feature Branch**: Push to `feature/awesome-feature` → Published as `npm-demo-release-please@1.0.0-feature-awesome-feature-1`

## Release Please Workflow

1. Make commits using conventional commit format
2. Release Please bot creates/updates a release PR
3. Review and merge the release PR
4. Package is automatically published to NPM

## Learn More

This demo repository is featured in the comprehensive guide: [**"The Ultimate Guide to NPM Release Automation: Semantic Release vs Release Please vs Changesets"**](https://oleksiipopov.com/blog/npm-release-automation/) - a detailed comparison of different NPM release automation tools with practical examples.
