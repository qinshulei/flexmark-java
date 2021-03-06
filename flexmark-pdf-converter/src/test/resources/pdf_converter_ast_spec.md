---
title: PdfConverter Extension Spec
author: 
version: 
date: '2016-06-06'
license: '[CC-BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/)'
...

---

## PdfConverter  

Converts pdf_converter text to PdfConverter nodes.

```````````````````````````````` example PdfConverter: 1
<p>Expected rendered HTML</p>
.
<html><head><style>
/* Table of contents */
@media print {
    .toc a::after {
      content: leader('. ') target-counter(attr(href), page) '.';
    }
}

.toc li { display: block }
ol.toc li:first-child { counter-reset: l1 }
ol.toc li li:first-child { counter-reset: l2; }
ol.toc li li li:first-child { counter-reset: l3 }
ol.toc li li li li:first-child { counter-reset: l4 }

ol.toc li:before { counter-increment: l1; content: counter(l1) ". " }
ol.toc li li:before { counter-increment: l2; content: counter(l1) "." counter(l2) ". " }
ol.toc li li li:before { counter-increment: l3; content: counter(l1) "." counter(l2) "." counter(l3) ". " }
ol.toc li li li li:before { counter-increment: l4; content: counter(l1) "." counter(l2) "." counter(l3) "." counter(l4) ". " }

/* Heading numbers */
body {counter-reset: h2}
h2 {counter-reset: h3}
h3 {counter-reset: h4}
h4 {counter-reset: h5}
h5 {counter-reset: h6}

h2:before {counter-increment: h2; content: counter(h2) ". "}
h3:before {counter-increment: h3; content: counter(h2) "." counter(h3) ". "}
h4:before {counter-increment: h4; content: counter(h2) "." counter(h3) "." counter(h4) ". "}
h5:before {counter-increment: h5; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". "}
h6:before {counter-increment: h6; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". "}

.nocount:before { content: ""; counter-increment: none } 

</style></head><body>
<p>Expected rendered HTML</p>
</body></html>
````````````````````````````````


```````````````````````````````` example PdfConverter: 2
<html><body>
<p>Expected rendered HTML</p>
</body></html>
.
<html><head><style>
/* Table of contents */
@media print {
    .toc a::after {
      content: leader('. ') target-counter(attr(href), page) '.';
    }
}

.toc li { display: block }
ol.toc li:first-child { counter-reset: l1 }
ol.toc li li:first-child { counter-reset: l2; }
ol.toc li li li:first-child { counter-reset: l3 }
ol.toc li li li li:first-child { counter-reset: l4 }

ol.toc li:before { counter-increment: l1; content: counter(l1) ". " }
ol.toc li li:before { counter-increment: l2; content: counter(l1) "." counter(l2) ". " }
ol.toc li li li:before { counter-increment: l3; content: counter(l1) "." counter(l2) "." counter(l3) ". " }
ol.toc li li li li:before { counter-increment: l4; content: counter(l1) "." counter(l2) "." counter(l3) "." counter(l4) ". " }

/* Heading numbers */
body {counter-reset: h2}
h2 {counter-reset: h3}
h3 {counter-reset: h4}
h4 {counter-reset: h5}
h5 {counter-reset: h6}

h2:before {counter-increment: h2; content: counter(h2) ". "}
h3:before {counter-increment: h3; content: counter(h2) "." counter(h3) ". "}
h4:before {counter-increment: h4; content: counter(h2) "." counter(h3) "." counter(h4) ". "}
h5:before {counter-increment: h5; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". "}
h6:before {counter-increment: h6; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". "}

.nocount:before { content: ""; counter-increment: none } 

</style></head><body>
<p>Expected rendered HTML</p>
</body></html>
````````````````````````````````


```````````````````````````````` example PdfConverter: 3
<html><head>
    <!-- other stuff -->
</head><body>
<p>Expected rendered HTML</p>
</body></html>
.
<html><head>
    <!-- other stuff -->
<style>
/* Table of contents */
@media print {
    .toc a::after {
      content: leader('. ') target-counter(attr(href), page) '.';
    }
}

.toc li { display: block }
ol.toc li:first-child { counter-reset: l1 }
ol.toc li li:first-child { counter-reset: l2; }
ol.toc li li li:first-child { counter-reset: l3 }
ol.toc li li li li:first-child { counter-reset: l4 }

ol.toc li:before { counter-increment: l1; content: counter(l1) ". " }
ol.toc li li:before { counter-increment: l2; content: counter(l1) "." counter(l2) ". " }
ol.toc li li li:before { counter-increment: l3; content: counter(l1) "." counter(l2) "." counter(l3) ". " }
ol.toc li li li li:before { counter-increment: l4; content: counter(l1) "." counter(l2) "." counter(l3) "." counter(l4) ". " }

/* Heading numbers */
body {counter-reset: h2}
h2 {counter-reset: h3}
h3 {counter-reset: h4}
h4 {counter-reset: h5}
h5 {counter-reset: h6}

h2:before {counter-increment: h2; content: counter(h2) ". "}
h3:before {counter-increment: h3; content: counter(h2) "." counter(h3) ". "}
h4:before {counter-increment: h4; content: counter(h2) "." counter(h3) "." counter(h4) ". "}
h5:before {counter-increment: h5; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". "}
h6:before {counter-increment: h6; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". "}

.nocount:before { content: ""; counter-increment: none } 

</style></head><body>
<p>Expected rendered HTML</p>
</body></html>
````````````````````````````````


```````````````````````````````` example PdfConverter: 4
<body>
<p>Expected rendered HTML</p>
</body>
.
<html><head><style>
/* Table of contents */
@media print {
    .toc a::after {
      content: leader('. ') target-counter(attr(href), page) '.';
    }
}

.toc li { display: block }
ol.toc li:first-child { counter-reset: l1 }
ol.toc li li:first-child { counter-reset: l2; }
ol.toc li li li:first-child { counter-reset: l3 }
ol.toc li li li li:first-child { counter-reset: l4 }

ol.toc li:before { counter-increment: l1; content: counter(l1) ". " }
ol.toc li li:before { counter-increment: l2; content: counter(l1) "." counter(l2) ". " }
ol.toc li li li:before { counter-increment: l3; content: counter(l1) "." counter(l2) "." counter(l3) ". " }
ol.toc li li li li:before { counter-increment: l4; content: counter(l1) "." counter(l2) "." counter(l3) "." counter(l4) ". " }

/* Heading numbers */
body {counter-reset: h2}
h2 {counter-reset: h3}
h3 {counter-reset: h4}
h4 {counter-reset: h5}
h5 {counter-reset: h6}

h2:before {counter-increment: h2; content: counter(h2) ". "}
h3:before {counter-increment: h3; content: counter(h2) "." counter(h3) ". "}
h4:before {counter-increment: h4; content: counter(h2) "." counter(h3) "." counter(h4) ". "}
h5:before {counter-increment: h5; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) ". "}
h6:before {counter-increment: h6; content: counter(h2) "." counter(h3) "." counter(h4) "." counter(h5) "." counter(h6) ". "}

.nocount:before { content: ""; counter-increment: none } 

</style></head><body>
<p>Expected rendered HTML</p>
</body>
</html>
````````````````````````````````


