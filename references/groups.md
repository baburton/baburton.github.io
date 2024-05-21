### Smart and Dynamic Groups

References now allows you to browse through **BibDesk smart groups** and
**JabRef dynamic groups**. These groups bring together references in your
BibTeX library based on rules.

BibDesk smart groups combine hand-crafted rules of different types (e.g., all
_@inproceedings_ papers with the keyword _geometry_). JabRef dynamic groups
either search for particular keywords in a chosen field, or use a free-form
search expression (e.g., _geometry and not distance_).

References goes to great lengths to apply these rules in exactly the same way
that BibDesk and JabRef do, and there is an automated suite of over 1800 tests
to ensure this. However, there will always remain a handful of cases where
References and BibDesk/JabRef differ. This page outlines some of the known
differences.

For BibDesk smart groups:

- **Crossref inheritance**: References (like BibTeX itself) allows entries to
  inherit fields through their crossrefs. Most of BibDesk's rules also look at
  these inherited fields, but its _Any Field_ rules only inherit some fields
  (not all).

- **The File field**: BibDesk allows rules based on local file attachments,
  which it encodes in its own _Bdsk-File-*_ fields. References supports not
  only the _Bdsk-File-*_ fields, but also the _File_ field (which some other
  apps use for local file attachments). References will look into both
  _Bdsk-File-*_ and _File_ fields when matching local file rules.

For JabRef dynamic groups:

- **Crossref inheritance**: As before, References allows entries to inherit
  fields through their crossrefs, whereas JabRef's dynamic group rules do not
  generally look at inherited fields.

- **Regular expressions**: JabRef allows regular expressions in its dynamic
  group rules, and References supports these. However, due to differences in
  the underlying programming languages, there are small variations in how
  these regular expressions behave, particularly with respect to accented
  symbols. For example, JabRef will not allow \w (a word character) to match
  an accented letter such as á, whereas References will; also, JabRef will not
  match Á with á in a case-insensitive regular expression, whereas References
  will.

- **Unicode symbols in searches**: JabRef tries to convert from TeX to unicode
  when it displays entries (e.g., it will convert the TeX {\"u} to the unicode
  symbol ü). In most cases, JabRef applies search rules to entries _after_
  this conversion has taken place. When processing JabRef dynamic groups,
  References uses its own TeX-to-unicode conversion process, which differs
  from JabRef's in many ways (see examples below). This decision is
  deliberate: it is technically infeasible to simulate JabRef's conversion
  precisely, and so by using References' conversion instead you will at least
  know what to expect (since you can already see the results of References'
  conversion within the app).

  - For simple cases such as accented letters (á) and simple mathematical
    symbols (ε), JabRef and References should give the same results.

  - For text with markup (e.g., typewriter text, superscripts, etc.), you
    should expect different results: here References uses standard unicode
    letters and applies the markup using font variations, whereas JabRef uses
    a separate collection of already-marked-up unicode symbols.

  - For more complex scenarios such as typesetting mathematical formulae, you
    should again expect the results to be different.

- **JabRef group hierarchies**: JabRef keeps its groups in a tree-like
  hierarchy, and allows _include groups_ (which also combine the members of
  their subgroups) and _refine groups_ (which apply their rules only to
  members of their supergroup). References does not support this hierarchy. If
  you open an include group or a refine group in References, it will clearly
  display the unsupported status of this group, and it will evaluate the group
  rules independently of any other groups in your library.

If you are aware of more differences then please contact the References
developer.
