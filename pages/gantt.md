---
layout: page
title: Gantt
permalink:
categories: [time management]
---



<script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/0.4.0/mermaid.full.js"></script>
<link rel="stylesheet" href="{{site.baseurl}}/css/mermaid.css">

<script>
        var mermaid_config = {
            startOnLoad:true
        }
        mermaid.startOnLoad = true;
        mermaid.sequenceConfig = {"diagramMarginX":50,"diagramMarginY":10,"actorMargin":50,"width":150,"height":45,"boxMargin":10,"boxTextMargin":5,"noteMargin":10,"messageMargin":35, "mirrorActors":false};
        mermaid.ganttConfig = {
            titleTopMargin:25,
            barHeight:20,
            barGap:4,
            topPadding:50,
            sidePadding:75,
            gridLineStartPadding:35,
            fontSize:11,
            numberSectionStyles:3,
            axisFormatter: [
                // Within a day
                ["%I:%M", function (d) {
                    return d.getHours();
                }],
                // Monday a week
                ["w. %U", function (d) {
                    return d.getDay() == 1;
                }],
                // Day within a week (not monday)
                ["%a %d", function (d) {
                    return d.getDay() && d.getDate() != 1;
                }],
                // within a month
                ["%b %d", function (d) {
                    return d.getDate() != 1;
                }],
                // Month
                ["%m-%y", function (d) {
                    return d.getMonth();
                }]
            ]
        };
</script>



## Chart


<div class="mermaid">
        gantt
        title A Gantt Diagram
        dateFormat  YYYY-MM-DD
        section Section
        A task           :a1, 2015-01-01, 3d
        Another task     :after a1  , 20d
        section Another
        Task in sec      :2015-01-12  , 12d
        booya			: 2015-01-13, 10d
        section Another2
        anther task      : 40d
        section Another3
        anther task      : 24d
        section Another4
        anther task      : 33d
        section Another5
        anther task      : 24d
        section Another6
        anther task      : 41d
        section Another7
        anther task      : 24d
        section Another8
        anther task      : 24d
        section Another9
        anther task      : 31d
        anther task      : 2d
        section Another10
        anther task      : 36d
        section Another11
        anther task      : 36d
        section Another12
        anther task      : 37d
</div>



## Code

{% highlight html %}
<div class="mermaid">
        gantt
        title A Gantt Diagram
        dateFormat  YYYY-MM-DD
        section Section
        A task           :a1, 2015-01-01, 3d
        Another task     :after a1  , 20d
        section Another
        Task in sec      :2015-01-12  , 12d
        booya			: 2015-01-13, 10d
        section Another2
        anther task      : 40d
        section Another3
        anther task      : 24d
        section Another4
        anther task      : 33d
        section Another5
        anther task      : 24d
        section Another6
        anther task      : 41d
        section Another7
        anther task      : 24d
        section Another8
        anther task      : 24d
        section Another9
        anther task      : 31d
        anther task      : 2d
        section Another10
        anther task      : 36d
        section Another11
        anther task      : 36d
        section Another12
        anther task      : 37d
</div>
{% endhighlight %}
