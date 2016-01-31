auto-complete-clang
===================

The AC sources for Clang. Requirements:

- clang
- auto-complete
- projectile.el

## Screenshot

![ac-clang](/../screenshot/ac-clang.png?raw=true "")

## Usage

  Here is an example config:

```lisp
(defun xwl-c-mode-common-hook ()
  (setq ac-sources (cons 'ac-source-clang ac-sources)))

(add-hook 'c-mode-common-hook 'xwl-c-mode-common-hook)
```

- Add additional project inlcude files?

  Setting the ac-clang-flags to include these additional include pathes. e.g.,

```lisp
(setq ac-clang-flags '("-I/path/to/project/inc"))
```

- integrate with cmake projects, see [cmake-compile-commands](https://github.com/xwl/cmake-compile-commands)
