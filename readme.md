PHP Guidelines
==============

These recommendations are exactly the same as [PHP-FIG] PSR-0, 1, 2 and PSR-4 standards, with two differences:

- you MAY use tabs for indenting
- you MAY write PHP constants `TRUE`, `FALSE`, and `NULL` in upper case

Basically, our standards are suitable for all PHP developers who want to be compliant
with well-known standards from the PHP-FIG, but are not interested in whitespace holy wars.

What standards are we talking about?
------------------------------------

- [PSR-0](accepted/PSR-0.md) - Autoloading Standard
- [PSR-1](accepted/PSR-1-basic-coding-standard.md) - Basic Coding Standard
- [PGS-2](accepted/PGS-2-coding-style-guide.md) - Coding Style Guide, replaces PSR-2
- [PSR-4](accepted/PSR-4-autoloader.md) - Improved Autoloader


Rationale
---------

Some people like tabs, some like spaces. The 30 % of PHP projects use tabs (including some PHP-FIG
member projects). We respect freedom of choice, especially when unsignificant whitespace can be converted
automatically, for example using Git:

```
git config --global filter.tabspace.smudge 'unexpand --tabs=4 --first-only'
git config --global filter.tabspace.clean 'expand --tabs=4 --initial'
```

(You should also configure Git to [convert line endings](https://help.github.com/articles/dealing-with-line-endings).)

Once chosen indentation is difficult to change, especially in bigger
projects, because such change will make it harder to deal with Git history, rebasing existing
branches and pull requests, etc.

Therefore standard [PGS-2](accepted/PGS-2-coding-style-guide.md) in comparsion to
the PSR-2 allows using tabs for indentation.

---

Whole [PHP documentation uses](http://php.net/manual/en/types.comparisons.php)
constants `TRUE`, `FALSE` and `NULL` written in upper case. PSR-1 itself
states that class constants MUST be in upper case. Therefore PGS-2 allows in comparsion
to the PSR-2 to write them in upper case too.

---

Using tabs or capital letters is matter of your choice. But you MUST use the same
style consistently across all files in whole vendor namespace.

[PHP-FIG]: http://www.php-fig.org
