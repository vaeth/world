# world

(C) Martin Väth (martin at mvath.de).
This project is under the BSD license 2.0 (“3-clause BSD license”).
SPDX-License-Identifier: BSD-3-Clause

__world__ is for the Gentoo __portage__ system to organize your `world` file
and to find installed packages or differences to `@world` (`--depclean`)

This project has several purposes:

1. It lets you save/restore your `world` file and compare with the backups
2. It can output your installed packages
3. It can output the packages which would be installed from `@world`,
   and it can compare them with 3.

For instance, the following is similar to `emerge --depclean`:
```
emerge --unmerge `world -2 test`
```

For more details, see the output of `world help`.

### Installation

For installation, copy `bin/*` with executable permission in your `$PATH`.
To obtain support for __zsh completion__, you can copy `zsh/*` to a
directory of yozr zsh's `$fpath`.

There is also an ebuild (`app-portage/world-mv`) in the mv overlay
(which is available over layman).
