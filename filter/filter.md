Filter
======




Convolve matrix
---------------

Have been doing some quick tests of this for emboss/bevel type effects.

It's not clear to me yet whether it operates on pixels in terms of screen/output or in drawing units - I think it might be the former.

Also firefox and chromium seem to disagree about filter order in some cases -- still investigating.

* Multiple filters have to be applied together in a single `filter:` declaration. Separate filter declarations across different style rules override earlier ones.
* Filter order **matters** - eg shadow before emboss looks weird
* Effects are contextual to the group - eg look at the effect of applying `emboss-first` to just the text compared to the applied to the whole group
* There are differences in drop-shadow rendering between ff and chromium when combined with the emboss. I think chromium is wrong - it gets lighter/fainter.



Shadow
------

https://css-tricks.com/adding-shadows-to-svg-icons-with-css-and-svg-filters/





Composite
---------

https://developer.mozilla.org/en-US/docs/Web/SVG/Reference/Element/feComposite


* over, in, atop, out, xor, lighter, arithmetic
