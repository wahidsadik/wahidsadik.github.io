---
layout: post
title: Trying out mermaid flowchart
tags: [math]
use_mermaid: true
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce eu lectus quis nibh hendrerit ultrices. Phasellus hendrerit, metus quis malesuada ultrices, metus est fringilla nibh, vitae porttitor tellus magna sed metus. Fusce et neque a nisi varius suscipit ac ut nisl. In posuere nulla in diam congue malesuada. Nulla varius aliquet velit, in condimentum urna efficitur a.

<!--more-->

Vivamus pretium tortor id fringilla aliquam. Nam nec ex non sem finibus dignissim vitae vitae enim. Aliquam egestas efficitur dolor at egestas. Aliquam efficitur tortor sollicitudin viverra vulputate. Proin massa est, sodales sit amet est eu, sodales pellentesque enim. Donec laoreet nisi leo, at vehicula velit commodo et. Sed vulputate elit tristique, vulputate velit quis, imperdiet magna. Vestibulum ex nunc, ornare eu vestibulum eget, egestas vitae massa. Quisque tempor nibh ex, quis vulputate libero interdum facilisis. Mauris hendrerit est tellus, vitae aliquam lectus congue posuere. Aliquam vitae orci dictum, euismod quam ac, sodales metus.

<div class="mermaid">
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
</div>

<div class="mermaid">
graph LR
    A[Square Rect] -- Link text --> B((Circle))
    A --> C(Round Rect)
    B --> D{Rhombus}
    C --> D
</div>
