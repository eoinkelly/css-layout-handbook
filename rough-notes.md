Outline

* intro
    * mention we are talking almost entirely about what is between the {} in CSS
    * I will work off the [CSS 2.2. spec](TODO) assuming that it is the most up to date version - even if it is not a CR yet
    * This is not a quick read. This is for when you are tired of not understanding CSS layout and want to take some time to build some foundational knowledge. If you have a particular CSS problem and a deadline there are many other great resources out there e.g. CSS tricks
    * mention the CSS properties we will learn about
        * display
        * position
        * box-sizing
        * top, bottom, left, right
        * float, clear
        * Small mention of the other things that create BFCs
    * what we will cover
        * foundational CSS knowledge that will allow you to understand the specs andthe tips you see online
    * we only cover things that matter in "reasonably modern" browsers
        * no IE quirks mode, no super old IE
    * we won't cover flexbox or grids
    * we won't cover specific "how to do two column layout with float"
        * there are plenty of that article already - see {examples}
* Small tapas of helpful knowledge
    * browser default CSS
        * note that there is no magic, just a built- in CSS file
        * show where to find it on various browser repos
* From DOM to boxes
    * take a DOM and work thorugh the story about how it converted into boxes
        * diff types of box
        * annotate each DOM node
            * num boxes created: 0-N

        * annotate the boxes with their "invisible properties scorecard" (similar to that "missing IPv4 packet" image)
            * properties phase 1:
                * positioning scheme for this box: normal-flow|floats|absolute-positioning
                * creates new block formatting context: yes|no
                * creates new stacking context: yes|no
                * creates new inline formatting context: yes|no
                * box type: inline-level|block-level
                * is replaced: yes|no
                * inline-level boxes only:
                    * is atomic inline level box: yes|no
                * block-level boxes only:
                    * is block-level box: yes|no
                    * is block container box: yes|no
                    * containing BFC established by: {ref to box}
                    * containing Stacking context established by: {ref to box}
                * is block container: yes|no
                    * NOTE: both inline-level and block-level boxes can be block containers
                    * QUESTION: does "block container" concept matter for our story?
                * containing block: {ref to box}
                    * NOTE: is usually the box created by the parent element in the DOM
            * properties phase 2:
                * box dimensions (decided by positioning scheme and CSS properties applied to box):
                    * content box:
                    * padding box:
                    * border box:
                    * margin box:
                    TODO: talk about box-sizing property as part of this
        * steps browser takes to go from DOM element to box
            1. gather CSS properties from all sources
                * built-in browser stylesheet
                * developer's stylesheets (provided by you)
                * user stylesheets (not super likely)
            1. Fill out the "properties phase 1" attributes
            1. Fill out the "properties phase 2" attributes
* inline formatting context
    * show the rules
    * work through an example
    * explain about anonymous block level boxes
* block formatting contexts
    * sources
        * CSS 2.1 spec
    * resources
        * https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context
            * re-states the spec
        * http://css-101.org/block-formatting-contexts/index.php
            * lets you play but just re-states spec
        * https://www.sitepoint.com/understanding-block-formatting-contexts-in-css/
            * quite good, explains how to achieve some layouts with them
        * http://yuiblog.com/blog/2010/05/19/css-101-block-formatting-contexts/
            * good but assumes a lot of knowledge
        * http://maxdesign.com.au/jobs/sample-block-formatting-context/index.htm
            * good examples but just re-states spec as explanation
        * http://tech.vg.no/2013/09/26/css-block-formatting-context/
            * explains how to use bfc to achieve certain layouts which are mostly obsoleted by flexbox
* stacking contexts


# Misc notes & ideas

* CSS overview in 2015: https://www.w3.org/TR/CSS/#css
    * current version of level 2 is CSS 2.1 but they are working on 2.2
        * 2.1: https://www.w3.org/TR/CSS2/
        * 2.2: https://www.w3.org/TR/CSS22/
            * FPWD april 2016
* the MDN docs do a good job of showing which specs influence which properties
    * WARN: parts of CSS 3 do augment some of the core CSS 2.1 stuff






