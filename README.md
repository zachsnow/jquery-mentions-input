jquery.mentionsInput
====================

This is a fork of Kenneth Auchenberg's `jquery.mentionsInput.js`.  I had
to hack in a bunch of tweaks and features for a project, and the result is
a version that is **API incompatible** with the original, but possibly useful
to some people. So here it is.

For more information on the original, checkout http://podio.github.com/jquery-mentions-input

New Features
------------

* A different, non-callback-based set of methods for accessing information about
  the mentions input.
* Reads an initial value from the `textarea`, parsing out mentions and
  prepopulating the mentions collection.  To do so it looks for text matching
  the output of the `mentionItemSyntax` template, so if you change that you
  should also change `mentionItemRegex`.
* Allows you to activate the autocomplete dialog using only @; to do so, simply
  set `minChars` to 0.
* Allows you to mention users multiple times, and doesn't just highlight the
  first text that matches a mentioned name.
* Added the option to not use `elastic` again (in my case the `textarea` was
  already using a different autogrow plugin).
* Make `<ESC>` close the autocomplete dialog.
