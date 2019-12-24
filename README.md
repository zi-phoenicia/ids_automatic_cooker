# IDS Automatic Cooker

## Layers of Unification

Layer 0: Glyphs considered different if they have different [CJK Strokes](https://en.wikipedia.org/wiki/CJK_Strokes_(Unicode_block)).
Exception: if two glyphs are not unified in Unicode, they're considered different. (e.g. 日 and 曰)
Exception of exception: if two glyphs are not unified by mistake, the latter one (with greater Unicode code point) is considered a duplication, and will be excluded from further processing. (e.g. 㶷 and 𤈎)

Layer 1: Glyphs considered identical, if they're only differnt in pre-defined stroke sets (e.g. 一 and ㇀ are identical, see l1_unifiable.txt)
Exception: if two glyphs are not unified, they're considered different. (e.g. 亠J and 丄)
Exception of exception: if two glyphs are not unified only because Source Separation Rule, they're considered identical. (e.g. 勻 and 匀)

Layer 2: Glyphs considered identical, if they're unified in Unicode.

Layer 3: Glyphs considered identical, if they're not unified only because Source Separation Rule.

## Files

l0_split_down.txt: all glyphs are split down into non-splittable components.

l0_unify.txt: this lists all cases in Exception of Layer 0.

l0_build_up.txt: this lists all glyphs built up by using build up rules.

l1_unifiable.txt: this includes all pre-defined stroke set, and glyphs unified only because Source Separation Rule.

l1_unify.txt: this includes all L0 Glyphs unified under pre-defined unifiable rules.

l1_merge_up.txt: this lists all L1 unifiable built up IDS.

l2_merge_up.txt: TBD

l3_unify.txt: TBD

l3_merge_up.txt: TBD
