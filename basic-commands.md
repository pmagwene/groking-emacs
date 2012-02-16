# Terminology

 * C-x -- ctrl-x
 * M-x -- "meta"-x (Esc)

# Help! I'm stuck

If you're stuck at a prompt or there's a long running process you can try the following:

 * Repeatedly type C-g
 * Hit the Esc key multiple times

# How do I quit?

 * C-x C-c (or command-Q on OS X gui version)

# Some useful commands

 * C-v move forward one screen
 * M-v move backward one screen
 * C-l clear screen and redisplay text (cycle cursor center->top->bottom)
 * M-> move to end of document
 * M-< move to beginning of document
 
# Examining values of variables
  
 * To find what value a variable is set to do: C-h v varname RET
 * To set value of a variable: M-x set-variable RET var RET value RET


# Getting help

 * Built in tutorial -- C-h t
 * Official manual C-h r
 
# Useful tutorials, tips, and guides

 * [Mastering Emacs](http://www.masteringemacs.org/)
 
# Initialization files

 * Here's a quote from the Emacs manual re: init files
 
> When Emacs is started, it normally tries to load a Lisp program from an initialization file, or init file for short. This file, if it exists, specifies how to initialize Emacs for you. Emacs looks for your init file using the filenames ~/.emacs, ~/.emacs.el, or ~/.emacs.d/init.el; you can choose to use any one of these three names (see Find Init). Here, ~/ stands for your home directory.

 * I'm using `~/emacs.d/init.el` which seems to be the more modern version.
 
 
# vim like key bindings

 * I like vim because it allows effective navigating from the home row
 
 * There are a number of vi/vim modes available for Emacs, including -- viper (default), vimpulse (no longer in development), and [evil](http://emacswiki.org/emacs/Evil)

 * I'm currently experimenting with evil, which seems pretty good!
 
