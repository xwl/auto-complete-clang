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

- integrate with cmake projects

  Add path of compile_commands.json to `ac-clang-cmake-compile-commands-json-files`.

```lisp
(setq ac-clang-cmake-compile-commands-json-files
      '(
        "/path/build/compile_commands.json"
        ))
```
