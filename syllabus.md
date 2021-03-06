---
layout: page
title: Syllabus
permalink: /syllabus/
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



### What?

* [Math 217: Multivariable and Vector Calcululs](https://courses.students.ubc.ca/cs/main?pname=subjarea&tname=subjareas&req=3&dept=MATH&course=217)
    * **Abstract:** Partial differentiation, extreme values, multiple integration, vector fields, line and surface integrals, the divergence theorem, Green's and Stokes' theorems. Intended for students in Honours Physics and Engineering Physics.
    * **Prerequisites:** A score of 68% or higher in one of PHYS 101, PHYS 107, PHYS 153, SCIE 001 and a score of 68% or higher in one of PHYS 102, PHYS 108, PHYS 153, SCIE 001 and a score of 68% or higher in one of MATH 101, MATH 103, MATH 105, MATH 121, SCIE 001.
    * [UBC Fizz Resources](http://www.ubcfizz.com/course-directory/math-courses/math-217-1)
    * [2015:M217 UBC Details](https://courses.students.ubc.ca/cs/main?pname=subjarea&tname=subjareas&req=5&dept=MATH&course=217&section=101)
*   [Lectures]( {{site.baseurl}}/index.html )
*   [Skills]( {{site.baseur}}/2015M217/categories/ )  <!-- including subdir is a hack. -->
*   [Concepts]( {{site.baseurl}}/tags/ )
* Text




### Where and When?

* [Schedule]( {{site.baseurl}}/pages/schedule.html)
    * Tuesdays, Thursdays: 9:30am -- 11:00am, [LSK (a.k.a. CSCI)](https://ssc.adm.ubc.ca/classroomservices/function/viewlocation?userEvent=ShowLocation&buildingID=LSK&roomID=201) 201
    * Wednesdays: 11:00am -- 12:00pm, [IBLC](https://ssc.adm.ubc.ca/classroomservices/function/viewlocation?userEvent=ShowLocation&buildingID=IBLC&roomID=182) 182
* Fall 2015:    Tuesday, September 8 -- Friday, December 4  
* Exams Interval:   Tuesday, December 8 -- Tuesday, December 22
*   [Academic Calendar](http://www.calendar.ubc.ca/vancouver/?page=deadlines)


### How?

* Assignments
* [Epics]( {{site.baseur}}/2015M217/epics/ )
* Midterm Exams
* Final Exam

### Who?

* Instructor: [Professor James Colliander](http://colliand.com)
* TA: Mingfeng Qiu




***



### Coarse View of Course

<div class="mermaid">
gantt
        dateFormat  YYYY-MM-DD
        title 2015M217

        section Administration
        Start Course                :crit, done, admin1, 2015-09-08, 1d
        Cr/D/F Grading Change Date  :crit, done, admin2, 2015-09-22, 1d
        Withdrawal Date             :crit, done, admin3, 2015-10-16, 1d
        End Course                  :crit, done, admin4, 2015-12-04, 1d

        section Class
        Vectors                     :crit, done, des1, 2015-09-08, 12d
        Differentiation		        :crit, done, des2, after des1, 28d
        Integration                 :crit, done, des3, after des2, 16d
        Vector Fields               :crit, done, des4, after des3, 24d

        section Exams
        Midterm1    :crit, mt1, 2015-10-15, 2d
        Midterm2	:crit, mt2, 2015-12-01, 2d
        Final		:crit, final1, 2015-12-10, 2d

        section Homework
        Assignments :crit, A1, 2015-09-08, 89d
        Epic1       :epic1, 2015-10-29, 2d
        Epic2       :epic2, 2015-11-23, 2d
  
</div>



### Fine View of Course
 
<div class="mermaid">
gantt
        dateFormat  YYYY-MM-DD
        title 2015M217

        section Administration
        Start Course                :crit, done, admin1, 2015-09-08, 1d
        Cr/D/F Grading Change Date  :crit, done, admin2, 2015-09-22, 1d
        Withdrawal Date             :crit, done, admin3, 2015-10-16, 1d
        End Course                  :crit, done, admin4, 2015-12-04, 1d

        section Vectors
        Intro                           :active, intro1, 2015-09-08, 1d
        Vectors                         :crit, done, des1, 2015-09-08, 12d
        3d                              :active, l1, after intro1, 1d
        dot and cross product           :active, l2, after l1, 2d
        cylinders and quadric surfaces  :active, l3, after l2, 2d
        vector functions                :active, l4, after l3, 3d
        motion in space                 :active, l5, after l4, 3d
        
        section Differentiation
        Differentiation                             :crit, done, des2, after des1, 28d
        functions of several variables              :active, l6, after l5, 5d
        limits                                      :active, l7, after l6, 3d
        continuity                                  :active, l8, after l7, 2d
        partial derivatives                         :active, l9, after l8, 5d
        linear approximiation                       :active, l10, after l9, 2d
        chain rule                                  :active, l11, after l10, 4d
        directional derivatives and the gradient    :active, l12, after l11, 2d
        Optimization                                :active, l13, after l12, 3d
        Lagrange multipliers                        :active, l14, after l13, 2d
        
        section Integration
        Integration                                 :crit, done, des3, after des2, 16d
        double integrals over rectangles            :active, l15, after l14, 2d
        double integrals over regions               :active, l16, after l15, 2d
        applications of double integrals            :active, l17, after l16, 3d
        triple integrals                            :active, l18, after l17, 5d
        triple integrals in spherical coordinates   :active, l19, after l18, 2d
        change of variables                         :active, l20, after l19, 2d
        
        section Vector Fields
        Vector Fields                                           :crit, done, des4, after des3, 24d
        vector fields and line integrals                        :active, l21, after l20, 2d
        line integrals of vector fields                         :active, l22, after l21, 2d
        conservative vector fields and path independence        :active, l23, after l22, 2d
        Green's theorem                                         :active, l24, after l23, 5d
        curl and divergence                                     :active, l25, after l24, 3d
        parametric surfaces                                     :active, l26, after l25, 2d
        surface integrals                                       :active, l27, after l26, 2d
        surface integrals of vector fields and Stokes theorem   :active, l28, after l27, 3d
        the divergence theorem                                  :active, l29, after l28, 3d

        section Exams
        Midterm1    :crit, mt1, 2015-10-15, 2d
        Midterm2	:crit, mt2, 2015-12-01, 2d
        Final		:crit, final1, 2015-12-10, 2d

        section Homework
        A1          :crit, A1, 2015-09-17, 4d
        A2          :crit, A2, 2015-09-23, 5d
        Epic1       :epic1, 2015-10-29, 2d
        A3          :crit, A3, 2015-11-02, 7d
        A4          :crit, A4, 2015-11-17, 5d
        Epic2       :epic2, 2015-11-23, 2d
        A5          :crit, A5, 2015-11-25, 7d
</div>




<!-- 
This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](http://jekyllrb.com/)

You can find the source code for the Jekyll new theme at: [github.com/jglovier/jekyll-new](https://github.com/jglovier/jekyll-new)

You can find the source code for Jekyll at [github.com/jekyll/jekyll](https://github.com/jekyll/jekyll) -->
