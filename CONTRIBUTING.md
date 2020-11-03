Contributing
============

Here are the guidelines we'd like you to follow:

* [Pull Request Submission Guidelines](#submit-pr)

## <a name="submit-pr"></a> Pull Request Submission Guidelines
Before you submit your pull request consider the following guidelines:

* Make your changes in a new git branch:

```shell
git checkout -b my-fix-branch master
```
* Follow the code style of the project, including indentation.
* Add or change the documentation as needed.
* Create your patch commit, **including appropriate test cases**.
* Run the test suites, and ensure that all tests pass.
* Commit your changes using a descriptive commit message. 

 ```shell
 git commit -a
 ```
Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

* Push your branch to GitHub:

   ```shell
   git push origin my-fix-branch
   ```
 
* In GitHub, create a pull request.
 
   Before creating a pull request, organize your [commits](#commits)
 
 * If we suggest changes, then:
 
   * Make the required updates.
   * Re-run the test suite to ensure tests are still passing.
   * Commit your changes to your branch (e.g. `my-fix-branch`).
   * Re-organize your [commits](#commits)
* Push the changes to GitHub (this will update your Pull Request).

You can also amend the initial commits and force push them to the branch.

```shell
git rebase master -i
git push origin my-fix-branch -f
```

This is generally easier to follow, but seperate commits are useful if the Pull Request contains
iterations that might be interesting to see side-by-side.

That's it! Thank you for your contribution!

### <a name="commits"></a> Commits

Commit messages must start with a capitalized and short summary (max. 50 chars)
written in the imperative, followed by an optional, more detailed explanatory
text which is separated from the summary by an empty line.

Commit messages should follow best practices, including explaining the context
of the problem and how it was solved, including in caveats or follow up changes
required. They should tell the story of the change and provide readers
understanding of what led to it.

If you're lost about what this even means, please see [How to Write a Git
Commit Message](http://chris.beams.io/posts/git-commit/) for a start.

In practice, the best approach to maintaining a nice commit message is to
leverage a `git add -p` and `git commit --amend` to formulate a solid
changeset. This allows one to piece together a change, as information becomes
available.

If you squash a series of commits, don't just submit that. Re-write the commit
message, as if the series of commits was a single stroke of brilliance.

That said, there is no requirement to have a single commit for a PR, as long as
each commit tells the story. For example, if there is a feature that requires a
package, it might make sense to have the package in a separate commit then have
a subsequent commit that uses it.

Remember, you're telling part of the story with the commit message. Don't make
your chapter weird.

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the master branch:

    ```shell
    git checkout master -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```