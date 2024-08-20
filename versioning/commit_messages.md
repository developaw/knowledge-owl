# (Commit) Message in a bottle

Imagine: You just finished writing the perfect piece of code. Spending hours - probably days - making it shiny and clean. Following all the best practices. Even adding some documentation! And you know. This code is ready to enter the world. You lean back. Ready to commit your code. Ready to commit you code? Oh no... you need a commit message... How to summarize the world changing code you just created? The blinking cursor jeers you. Your head is blank. It feels like the world is waiting for your genius commit message. Your fingers move carefully and slowly across the keyboard. You start typing. Quickly. "new stuff". Commit. Push. And that's it.

Can you relate to that? Than you're probably not alone.

## Why good commit messages matter

But well-written and meaningful commit messages can be of advantage. They help you, future-you and other developers to understand what and how you built your project. And they help you to work faster. If you have a consistent structure of commit messages, you can automatically create changelogs or software versions. You could also automatically trigger build and publish processes.

## Conventional Commits

Luckily there already is a specification that helps to create better commit messages: Conventional Commits. Sometimes this specification is also referred to as semantic commits.

### Structure of Conventional Commits

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```  


Example:
```
feat(auth): add new authentication role

Add role of 'Witch' - a role that magically gets access to every page

Refs: TICKET-1337
```  

#### Types

The `type` is mandatory and gives a first hint on what the commit contains. The following types are defined in the Conventional Commit:

* `feat` - introducing/removing a new feature
* `fix` - repairing a bug
* `build` - adding/updating build system or external dependencies
* `chore` - updating internal code, no production code change (e.g. initial commit, change `.gitignore`)
* `ci` - changing CI configuration
* `docs` - adding/updating documentation
* `style` - updating the code without changing the meaning (formatting, white-spaces, &c.)
* `refactor` - refactoring code
* `perf` - improving performance
* `test` - adding/updating tests

Sidenote: If you're more the picture-type, you could think about using [gitmoji](https://gitmoji.dev/) as types.

#### Scope

The `scope` is optional. It gives more information about where in the code the change is located. This could be a topic like `authentication` or even a file like `auth-roles.ts`.

#### Description

In addition to the `type`, the `description` is also mandatory. It is in an on point summary of what the commit contains.

#### Body

The `body` is reserved for providing additional contextual information like a motivation or a more detailed description of the commit. The `body` is optional.

#### Footer

The `footer` is also optional. Each commit message can have various footers. Each footer starts with a word token, followed by either a `: ` (or ` #` separator) and afterwards a string.

Footer tokens can be e.g. `Refs`, `Closes`, `Acked-by`

If you want to add a ticket number to your commit message. You can use the footer for that.

#### Breaking Change

Breaking Changes can be introduced in two ways. Either with an `!` after the `scope` and right before the `:` or with a footer that has `BREAKING CHANGE` as a token and is followed by `:`.

### Tense of description/body-texts
The Conventional Commit specification doesn't include rules about the tense for the description or the body text.

Normally you find the texts in simple present or in the will-future.

For the simple present form imagine that the text would start with `The commit`. The describing verb then would be something like `adds`.

```
feat(auth): adds new authentication role
```

In the will-future form the text would start with `The commit will`. The describing verb then would be something like `add`.

```
feat(auth): add new authentication role
```

I personally prefer the will-future form. But I also think it's something where you can adapt to the majority of the team.

### Conventional Commit in IntelliJ
If you're using an IntelliJ product and you want a little bit support with your conventional commit message. I can recommend the Conventional Commit plugin from Edoardo Luppi. See
https://plugins.jetbrains.com/plugin/13389-conventional-commit

## Sources
* https://www.conventionalcommits.org/en/v1.0.0/
* https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13
* https://dev.to/safdarali/good-commit-vs-your-commit-how-to-write-a-perfect-git-commit-message-59ol
