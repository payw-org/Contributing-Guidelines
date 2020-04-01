# PAYW Contributing Guidelines

Please follow these guidelines when you are trying to contribute to PAYW software.

## Language

We **_prefer English over Korean_** due to its globally high usage and impact. So it is strongly recommended to use English throughout your development routine. Don't worry about your bad English. We don't judge any kind of your grammar or language structure including ours. However, it is important to make sure that each sentence you wrote should be easily understandable and has an exact atomic meaning without ambiguity.

## Code editor

If there exists a specific code editor configuration inside a repository, we recommend you to use that editor. For example, if there is `.vscode` folder, please use **Visual Studio Code**. Or if there is `.idea` folder, please use **JetBrains**' IDE.

## Code formatting

Keep your codes clean and **_consistent_** using code formatters and linters. Most of the time formatting and linting would've already been set by default in each repository. And sometimes you should use the specific code editor to match the configuration.

## Naming

### Casing

**Files**

| Language   | Case         | Example          |
| ---------- | ------------ | ---------------- |
| JS/TS      | `kebab-case` | `get-state.ts`   |
| components | `PascalCase` | `Navigation.tsx` |

**HTML/CSS**

- `kebab-case`

**JavaScript/TypeScript**

| Type    | Case         |
| ------- | ------------ |
| classes | `PascalCase` |
| others  | `camelCase`  |

**React/Vue Components**

- `PascalCase`

**MySQL table attributes**

- `snake_case`

### Do naming as long as enough to explain

### Make naturally readable

Always prefix functions and methods with a verb. Then sequentially make the name like a sentence.

### Booleans

If a variable is a boolean, prefix the variable name with `is`. For example,

```ts
let isAvailable = false
let isGoingTo
```

## Git commit messages

Generally there are two acceptable styles of commit message. We follow the best conventions to keep a git repository and its history as neat as possible.

### commit type: what you did in present-tense, imperative-style

Refer to [here](http://karma-runner.github.io/0.10/dev/git-commit-msg.html) and [here](https://seesparkbox.com/foundry/semantic_commit_messages) for more information.

**Available types**

- chore (updating grunt tasks etc; no production code change)
- docs(or doc) (changes to documentation)
- feat (new feature)
- fix (bug fix)
- refactor (refactoring production code)
- style (formatting, missing semi colons, etc; no code change)
- test (adding missing tests, refactoring tests; no production code change)
- deps (anything related to dependencies)

**Examples**

- `chore: add Oyster build script`
- `doc: explain hat wobble`
- `feat: add beta sequence`
- `fix: remove broken confirmation message`
- `refactor: share logic between 4d3d3d3 and flarhgunnstow`
- `style: convert tabs to spaces`
- `test: ensure Tayne retains clothing`
- `deps: bump dependencies`

> You can also use other types like `misc:`, `design:`, `types:` or whatever that fit well with your works.

### Start with a present-tense verb in imperative-style with a first character in uppercase

**Examples**

- `Update README.md`
- `Add assets`

## Pull Requests

## Versioning

We are following the [SemVer](https://semver.org/) but in a much simpler and restricted way.

### Backwards Compatible

It means that your code written on a new version should run on the previous backwards compatible versions without any modification.

### x.y.Z (Patch version)

- Fix backwards compatible bugs

### x.Y.z (Minor version)

- Introduce new backwards compatible functionality
- Deprecate functionality

### X.y.z (Major version)

- Introduce any backwards incompatible changes

### Pre-release version

In a form of `x.y.z-keyword.n`

**Examples**

- `1.0.0-alpha.1`
- `2.0.0-beta.3`
