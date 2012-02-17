The text below is from [this link](http://xahlee.blogspot.com/2010/09/difference-between-emacss-getenv-path.html).

* When you start emacs from a shell, emacs inherits shell's environment variables. (true on Windows, Mac, Linux)

* On Windows, when you start emacs from GUI, emacs also inherit environment variables, from the Registry.

* On Mac OS X, when you start emacs from GUI, emacs does not inherit environment variables from your shell, but does inherit the system-wide environment variables from 〔~/.MacOSX/environment.plist〕.


Emacs has a variable named “exec-path”. Its value is a list of dir paths. Emacs uses “exec-path” to find executable binary programs. For example, when spell checking, emacs will try to find ispell or aspell in exec-path. 

# Difference between "exec-path" and "PATH"

The value of `PATH` is used by emacs when you are running a shell in emacs, similar to when you are using a shell in a terminal.

The `exec-path` is used by emacs itself to find programs it needs for its features, such as spell checking, file compression, compiling, grep, diff, etc.

If you did set the PATH env var within emacs, you probably also want to adjust your `exec-path`. Here's a example of setting exec-path:

~~~
(when (string-equal system-type "windows-nt")
  (setq exec-path
'(
"C:/Program Files (x86)/Emacs/emacs/bin/"
"C:/Program Files (x86)/Emacs/EmacsW32/gnuwin32/bin/"
"C:/Windows/system32/"
"C:/Windows/"
"C:/Windows/System32/Wbem/"
"C:/Windows/system32/WindowsPowerShell/v1.0/"
)
 ))
~~~

The value of `(getenv "PATH")` and `exec-path` do not need to be the same.

---

