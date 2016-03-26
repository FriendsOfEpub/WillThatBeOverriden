# KF8

Easy one. We’ve got some kind of “ePub 2.5” format there, with very few alterations and undocumented support of `-webkit-` prefixed properties as a bonus.

Now, there is one important thing which is worth reporting…

**If part of a CSS declaration (prop OR value) is not supported, the whole is erased.**

In other words, should have Amazon added support for say `max-width` at any time in the life of KF8, the declaration would still have been **missing in your converted CSS.** Same for value `inherit`, etc.

If I’m usually trying to stay objective—and that's obviously not easy—, this small detail speaks volumes to me. It feels like their whole ~~system~~ ~~mess~~ gas-works isn’t even future-proof. 

“Need update? Create format.” 

Also, KindleGen doesn’t know how to parse `<header>`. 