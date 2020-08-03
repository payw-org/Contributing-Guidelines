# PAYW Contributing Guidelines

Please follow these guidelines when you are trying to contribute to PAYW software. Many parts are related to JavaScript/TypeScript because we mostly use them in our project.

## Language

We **_prefer English over Korean_** due to its globally high usage and impact. So it is strongly recommended to use English throughout your development routine. Don't worry about your bad English. We don't judge any kind of your grammar or language structure including ours. However, it is important to make sure that each sentence you wrote should be easily understandable and has an exact atomic meaning without ambiguity.

## Code editor

If there exists a specific code editor configuration inside a repository, we recommend you to use that editor. For example, if there is `.vscode` folder, please use **Visual Studio Code**. Or if there is `.idea` folder, please use **JetBrains**' IDE.

## Code formatting

Keep your codes clean and **_consistent_** using code formatters and linters. Most of the time formatting and linting would've already been set by default in each repository. And sometimes you should use the specific code editor to match the configuration.

## Code Style

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

Don't worry about longer variable names. Eventually they're going to be mangled and ultimately shortened by compressors or obfuscators. It is important to make the variable names meaningful so that anyone can understand what those are doing without reading the whole documentation.

```ts
const someValuesDifferentFromPreviousOne = {}

function hastilyRunAwayWhenThereIsMonsterBehindMe() {}
```

> These are some jokey examples and it doesn't mean you always have to do like this.

### Make naturally readable

Functions are things **doing** something. So try to prefix functions and methods with a verb. Then sequentially make them readable like a sentence.

For example,

```ts
function sayHello() {}
const sayGoodbye = () => {}

class Baby {
  isCute = true

  growUp() {}
}
```

### Booleans

If a variable is a boolean, prefix the variable name with verbs like `is` or `has` that implicates two states(`true` or `false`) of what it's saying.

For example,

```ts
let isAvailable = false
let isGoingToJump = true

let hasWeapon = true
let hasGone = false

let willChange = true
let willDisappear = false
```

> Again, the same discipline applies here to make them naturally readable.

### Line break between different scopes

**Examples**

- TypeScript

```ts
const log = console.log
const condition = 5 < 7
// Line break
if (condition) {
  log('5 is smaller than 7')
}
// Line break
const people = ['Kevin', 'Harry', 'Justin']
// Line break
for (const person of people) {
  log(person)
}
```

- Sass

```scss
body {
  display: grid;
  // Line break
  footer {
    position: relative;
  }
}
```

> Two or more sequential line breaks are not allowed by Prettier. They will be automatically reduced to one.

## Git branch names

Categorize by a slash(`/`) then concatenate with a dash(`-`).

For example,

```
feat/fire-alarm

feat/swimming-pool

refactor/rename-variables

fix/wrong-type-declarations
```

## Git commit messages

Generally there are two acceptable styles of commit message. We follow the best conventions to keep a git repository and its history as neat and consistent as possible.

### `commit type: what you did in present-tense, imperative-style`

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

When you make a pull request, explain what you did and what has been changed in detail.

## Versioning

We are following the [SemVer](https://semver.org/) but in a much simpler and restricted way.

**Backwards Compatible** means that your code written on a new version should run on the previous backwards compatible versions without any modification.

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
