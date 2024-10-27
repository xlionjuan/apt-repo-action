# create-apt-repo

## Forked from [morph027/apt-repo-action](https://github.com/morph027/apt-repo-action) and did following changes

Please give him credit and stars.

* Do not rely on Ubuntu's system environments (Del any `apt-get` stuffs)
* Do not generate keyring `.deb` because preorganized `.list` or `.sources` is more preferred
* Delete import function because not needed for me and can't achieved on Fedora systems
* `reprepro-multiple-versions` -> `reprepro` because it isn't needed and not existed in Fedora repo

## Why?

Because I created RustDesk APT and RPM repos, and I need to get latest `wget2` and [createrepo_c](https://github.com/rpm-software-management/createrepo_c), so I created [xlionjuan/fedora-createrepo-image](https://github.com/xlionjuan/fedora-createrepo-image).

I can get some benefits from it:

* Consistency
* Time, resources and energy saving, because these actions run's everyday, it won't need to update package lists and install dependencies every times when it runs.
* Some benefits from `wget2`