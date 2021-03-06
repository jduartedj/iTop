# Contributing to iTop

You want to contribute to iTop? Many thanks to you! 🎉 👍

Here are some guidelines that will help us integrate your work!


## Contributions

### Subjects
You are welcome to create pull requests on any of those subjects:

* 🐛 `:bug:` bug fix
* 🔒 `:lock:` security
* 🌐 `:globe_with_meridians:` translation

If you want to implement a **new feature**, please [create a corresponding ticket](https://sourceforge.net/p/itop/tickets/new/) for review.   
If you ever want to begin implementation, do so in a fork, and add a link to the corresponding commits in the ticket. 

### License
iTop is distributed under the AGPL-3.0 license (see the [license.txt] file), 
your code must comply with this license.

If you want to use another license, you may [create an extension][wiki new ext].

[license.txt]: https://github.com/Combodo/iTop/blob/develop/license.txt
[wiki new ext]: https://www.itophub.io/wiki/page?id=latest%3Acustomization%3Astart#by_writing_your_own_extension


## Branch model

TL;DR:
> **create a fork from iTop main repository,  
> create a branch based on either release branch if present, or develop otherwise**

We are using the [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/) branch model. That means we have in our repo those 
main branches:

- develop: ongoing development version
- release/*: if present, that means we are working on a beta version
- master: previous stable version

For example, if no beta version is currently ongoing we could have:

- develop containing 2.8 version
- master containing 2.7 version

In this example, when 2.8 beta is shipped that will become:

- develop: 2.9 version
- release/2.8: 2.8 beta
- master: 2.7 version

And when 2.8 final will be out:

- develop: 2.9 version
- master: 2.8 version


## Coding

### PHP styleguide

Please follow [our guidelines](https://www.itophub.io/wiki/page?id=latest%3Acustomization%3Acoding_standards).

### Tests

Please create tests that covers as much as possible the code you're submitting.

Our tests are located in the `test/` directory, containing a PHPUnit config file : `phpunit.xml.dist`.

### Git Commit Messages

* Describe the functional change instead of the technical modifications
* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or less
* Please start the commit message with an applicable emoji (following the [Gitmoji guide](https://gitmoji.carloscuesta.me/).). For example :
    * 🌐 `:globe_with_meridians:` for translations
    * 🎨 `:art:` when improving the format/structure of the code
    * ⚡️ `:zap:` when improving performance
    * 🐛 `:bug:` when fixing a bug
    * 🔥 `:fire:` when removing code or files
    * 💚 `:green_heart:` when fixing the CI build
    * ✅ `:white_check_mark:` when adding tests
    * 🔒 `:lock:` when dealing with security
    * ⬆️ `:arrow_up:` when upgrading dependencies
    * ⬇️ `:arrow_down:` when downgrading dependencies
    * ♻️ `:recycle:` code refactoring
    * 💄 `:lipstick:` Updating the UI and style files.

## Pull request

When your code is working, please:

* stash as much as possible your commits,
* rebase your branch on our repo last commit,
* create a pull request.

Detailed procedure to work on fork and create PR is available [in GitHub help pages](https://help.github.com/articles/creating-a-pull-request-from-a-fork/).
