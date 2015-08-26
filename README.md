# 4d-tips-html-to-text
Examples of how to convert HTML to text in 4D

Solution 1: JavaScript
---

```
$HTML:=OBJECT Get pointer(Object named;"HTML")
$Text:=OBJECT Get pointer(Object named;"Text")

WA SET PAGE CONTENT(*;"WebKit";$HTML->;"")
$Text->:=WA Evaluate JavaScript(*;"WebKit";"document.body.innerText";Is text)
```
