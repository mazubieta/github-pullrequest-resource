# v26 @ 8/21/2017

* Support evaluating the concourse BUILD environment variables in a context.

# v25 @ 8/1/2017

* support caching of API requests to Github. This decreases hitting the
rate limit per hour. It does not reduce the number of request, though.

# v24 @ 6/26/2017

* `README.md` updates from @cjcjameson and @richarddowner
* Add support for `git-lfs`

# v23 @ 3/9/2017

* update LICENSE file
* support filtering PRs with a specific `label`

# v22 @ 3/1/2017

* remove default `--depth 1` when none is specified

# v21 @ 2/27/2017

* support multiple `contextes` in a single `put`
* specify `depth` and `submodule` on a `git clone`
* fix typo in README [Thanks @trizko](https://github.com/jtarchie/pullrequest-resource/pull/57)
* fix issue with Github API proxying [Thanks @databus](https://github.com/jtarchie/pullrequest-resource/pull/56)

# v20 @ 12/17/2016

* disable PRs that were made from forks with `disable_forks` [Thanks @henrytk](https://github.com/jtarchie/pullrequest-resource/issues/43)
* PRs only trigger when matching `paths` or `ignore_paths` [Thanks @ahume](https://github.com/jtarchie/pullrequest-resource/issues/42)
* refactored so adding filters is easier and testable
* finally deprecated `every`, you should always be using `version: every`

# v19 @ 12/6/2016

* add meta field for target branch `basebranch` (Thanks @arwineap)

# v18 @ 12/4/2016

* No new features. This was a refactor, which I'd like to production test. If
you need to revert please lock the `resource_type` to the `v17` tag.

# v17 @ 9/27/2016

* document the `base` option
* improve deprecation warning to be conditional (Thanks @jmcarp)

# v16 @ 9/13/2016

* Fix issue where `git submodule` was not being called on the PR branch

# v15 @ 9/11/2016

* Resolve issue where `every` was returning PRs incorrect order. [Issue #27](https://github.com/jtarchie/pullrequest-resource/issues/27)
* Resolve issue when a PR made on the `master` branch could not be checked out. [Issue #33](https://github.com/jtarchie/pullrequest-resource/issues/33)

# v14 @ 9/8/2016

* Create a comment on a pull request. [PR #24](https://github.com/jtarchie/pullrequest-resource/pull/24)
* Only iterate over pull requests that were made against a specific branch. [PR #25](https://github.com/jtarchie/pullrequest-resource/pull/25)
* Pull in the merged version of the pull request. This is useful to make sure it is mergeable with the current branch. [PR #29](https://github.com/jtarchie/pullrequest-resource/pull/29)

# v13 @ 7/23/2016

* The `every` flag can be set on `source`. This removes the need to always set a status on
a PR, which helps with the iteration. Consider this *beta*, please comment on this [issue](https://github.com/jtarchie/pullrequest-resource/issues/15).

* Pulled [git resource](https://github.com/concourse/git-resource) configuration steps for `in`.
  * username - Username for HTTP(S)
	* password - Password for HTTP(S)
	* skip_ssl_verification - Skips git ssl verification
	* git_config - key value pairs for `git config`

# v12 @ 5/25/2016

* The branch of the checked out PR will be the original name of from the PR. (Thomas and Benjamin)
