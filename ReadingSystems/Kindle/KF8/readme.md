# KF8

Easy one. It feels like we’ve got some kind of “ePub 2.5” format there, with few alterations and undocumented support of `-webkit-` prefixed properties as a bonus.

Actually, things are a bit more complicated. 

KF8 can be considered the foundation for KFX; it works the same at the fundamental level.

Here is what happens: 

1. contents are cut into fragments (with the corresponding attributes, styles, etc.);
2. the renderer is just an HTML skeleton;
3. fragments are then re-injected into this skeleton at runtime.

If you unpack a Kindle Mobi file using Kindle/Mobi Unpack, the app is actually rebuilding the EPUB file bu re-injecting those fragments into the skeleton.

Now, there is another important thing which is worth reporting…

**If part of a CSS declaration (prop OR value) is not supported, the whole is erased.**

In other words, should have Amazon added support for say `max-width` at any time in the life of KF8, the declaration would still have been **missing in your converted CSS.** Same for value `inherit`, etc.

If I’m usually trying to stay objective—and that's obviously not easy—, this small detail speaks volumes to me. It feels like their whole ~~system~~ ~~mess~~ gas-works isn’t even future-proof. 

“Need update? Create format.” 

Also, KindleGen doesn’t know how to parse `<header>`. 