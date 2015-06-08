---
layout: page
title: Schedule
permalink:
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






### Coarse View of Course

<!-- <div class="mermaid">
gantt
		vectors  2015-09-08, 12d
		partial derivatives 2015-09-20, 26d
		integration 2015-10-16, 14d
		vector fields 2015-11-01, 26d
</div> -->


 
<div class="mermaid">
gantt
        dateFormat  YYYY-MM-DD
        title 2015M217

        section Preparation
        Jekyll Site     :active, web1, 2015-05-28, 10d
        Organize Lectures   :active, web2, after web1, 20d
        Plan Assessments    :crit, after web1, 25d

        section Class
        Vectors            	:crit, done,    des1, 2015-09-08, 12d
        Differentiation		      :crit, done, des2, after des1, 25d
        Integration               :crit, done, des3, after des2, 14d
        Vector Fields               :crit, done, des4, after des3, 35d

        section Exams
        Midterm1	:crit, mt1, 2015-10-04, 2d
        Midterm2	:crit, mt2, 2015-11-15, 2d
        Final		:crit, final1, 2015-12-12, 2d

        section Homework
        A          :crit, A1, 2015-09-08, 89d
        EPIC1       : epic3, 2015-10-09, 2d
        EPIC2       : epic4, 2015-11-12, 2d
  
</div>



### Fine View of Course
 
<div class="mermaid">
gantt
        dateFormat  YYYY-MM-DD
        title 2015M217


        section Vectors
        Intro     :active, intro1, 2015-09-08, 1d
        Vectors             :crit, done,  des1, 2015-09-08, 12d
        3d                  :active, l1, after intro1, 1d
        dot and cross product :active, l2, after l1, 2d
        cylinders and quadric surfaces  :active, l3, after l2, 2d
        vector functions   :active, l4, after l3, 3d
        motion in space   :active, l5, after l4, 3d
        
        section Differentiation
        Differentiation           :crit, done, des2, after des1, 25d
        functions of several variables  :active, l6, after l5, 5d
        limits   :active, l7, after l6, 3d
        continuity :active, l8, after l7, 2d
        partial derivatives  :active, l9, after l8, 5d
        linear approximiation  :active , l10, after l9, 2d
        chain rule  :active, l11, after l10, 4d
        directional derivatives and the gradient :active, l12, after l11, 2d
        Optimization :active, l13, after l12, 3d
        Lagrange multiplies :active, l14, after l13, 2d
        
        section Integration
        Integration               :crit, done, des3, after des2, 18d
        double integrals over rectangles :active, l15, after l14, 2d
        double integrals over regions  :active, l16, after l15, 2d
        applications of double integrals  :active, l17, after l16, 3d
        triple integrals   :active, l18, after l17, 5d
        triple integrals in spherical coordinates  :active, l19, after l18, 2d
        change of variables   :active, l20, after l19, 2d
        
        section Vector Fields
        Vector Fields               :crit, done, des4, after des3, 24d
        vector fields and line integrals    :active, l21, after l20, 2d
        line integrals of vector fields     :active, l22, after l21, 2d
        conservative vector fields and path independence    :active, l23, after l22, 2d
        Green's theorem    :active, l24, after l23, 5d
        curl and divergence    :active, l25, after l24, 3d
        parametric surfaces    :active, l26, after l25, 2d
        surface integrals   :active, l27, after l26, 2d
        surface integrals of vector fields and Stokes theorem   :active, l28, after l27, 3d
        the divergence theorem   :active, l29, after l28, 3d

        section Exams
        Midterm1    :crit, mt1, 2015-10-04, 2d
        Midterm2    :crit, mt2, 2015-11-15, 2d
        Final       :crit, final1, 2015-12-12, 2d

        section Homework
        A1         :crit, A1, 2015-09-10, 7d
        A2         :crit, A2, after A1, 7d
        A3         :crit, A3, after A2, 7d
        A4         :crit, done, A4, after A3, 7d
        A5         :crit, A5, after A4, 7d
        EPIC1       :epic1, after A5, 2d
        A6         :crit, A6, after A5, 7d
        A7         :crit, A7, after A6, 7d
        A8         :crit, A8, after A7, 7d
        A9         :crit, A9, after A8, 7d
        A10        :crit, done, A10, after A9, 7d
        A11        :crit, A11, after A10, 7d
        EPIC2       : epic2, after A10, 2d 
        A12         :crit, A12, after A11, 7d  
</div>

