# Documentation Pull Request Acceptance Workflow

## One Time Setup
* [Fork](https://help.github.com/articles/fork-a-repo/) the
[tutorial](https://github.com/eclipse-ee4j/jakartaee-tutorial/) repository.
* [Clone](https://help.github.com/articles/cloning-a-repository/)
your forked repository.
```
$ git clone https://github.com/YOUR-USERNAME/jakartaee-tutorial.git
```
* [Configure](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
the remote for your fork.
```
$ git remote add upstream https://github.com/eclipse-ee4j/jakartaee-tutorial.git
$ git remote -v
origin    https://github.com/YOUR-USERNAME/jakartaee-tutorial.git (fetch)
origin    https://github.com/YOUR-USERNAME/jakartaee-tutorial.git (push)
upstream    https://github.com/eclipse-ee4j/jakartaee-tutorial.git (fetch)
upstream    https://github.com/eclipse-ee4j/jakartaee-tutorial.git (push)
```
## Raising a Pull Request
* Sync the master of your fork with upstream master.
```
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
$ git push origin master # push local master to github fork.
```
* Create a local topic branch in your fork from your master.
```
$ git checkout -b doc_update
```
* Do the development in your branch.
* Commit all the changes.
```
$ git add src/main/jbake/content/my.adoc
$ git commit -m "my commit message"
```
* Push your changes in a remote branch of your fork.
```
$ git push origin doc_update
```
* Before raising a Pull Request, please raise an
[issue](https://github.com/eclipse-ee4j/jakartaee-tutorial/issues)
if it doesn't exist. We would like every Pull Request to be associated
with an issue. Submit the Pull Request referring to the issue number.
* Raise a [Pull Request](https://github.com/eclipse-ee4j/jakartaee-tutorial/pulls).
* Make sure you put a proper 'title' for the Pull Request. The title of
the Pull Request would become the commit message. Instead of giving
'title' like "Iss xxxx" or "Fixes #xxxxx", consider giving a proper one
line 'title' for the Pull Request like "Fixes xxx : <brief description
about the issue/fix>"
* In the Pull Request description (body), please mention "Fixes #xxxxx"
in order to link the Pull Request with the Issue you are fixing.
* If you have signed the [ECA](https://www.eclipse.org/legal/ECA.php),
one of the project team members will review your Pull Request.
