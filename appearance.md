
# line wrapping

There are various line wrapping modes availabe in Emacs. 

For editing texts, I like it if lines are unbroken in terms of the file, but are broken in terms of visual presentation.  To achieve you can you `visual-line-mode`.  To do so automatically when you are in text mode, add the following to `init.el`:

~~~
(add-hook 'text-mode-hook 'turn-on-visual-line-mode)
~~~

Alternately, if you have visual-line-mode turned off, and you want to reformat text nicely with hard returns you can use `M-q` which issues the `fill-paragraph` command.

