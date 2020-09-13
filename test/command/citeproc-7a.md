```
% pandoc --citeproc -t markdown-citations
---
csl: command/chicago-fullnote-bibliography.csl
references:
  - id: test
    title: Test
    author:
      family: Doe
      given: John
---

Test [@test, 12].

Test [@test, 12].

Test.^[asdfasdf]

Test [@test, 12].
^D
Test.[^1]

Test.[^2]

Test.[^3]

Test.[^4]

::: {#refs .references .hanging-indent}
::: {#ref-test}
Doe, John. "Test," n.d.
:::
:::

[^1]: John Doe, "Test," n.d., 12.

[^2]: Ibid.

[^3]: asdfasdf

[^4]: Doe, "Test," 12.
```