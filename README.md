# Html5-Css-Jonas

# Sec3 Css Fundamentals

## 28. Psudo classes

    li:first-child:
        first child of a list

    li:last-child:
        last child of a list

    li:nth-child(2):
        second child

    li:nth-child(odd):
        selects the odds in the list order

    article p:last-child :
        selects article paragraphs last child

if we mix multiple elements inside of a parent elememt the psudo classes dont work so well

    article p:first-child :
        dosent work with our html because there are multiple element types inside of parent

## 29. Styling Hyperlinks

    a {
        color: #103333
    }

above works but its not good practice, instead we should target a psudo element that will allow us to target state

    a:link { // this way we select only a tags that have hrefs in them
        color: #999
    }

    a:visited { // visited links
        color: #999
    }


    a:hover { // makes changes on hover
        color: orangered:
        font-weight: bold;
        text-decoration: underline dotted orangered:
    }

    a:active { // during duration of the click
        background-color: black; font-style: italic;
        }

## 31. Css Theory#1: Conflicts Between Selectors

### Resolving Conflicting Declarations

    Highest Priority

        5 Declarations marked !imporntant (not good practice generally)

        4 Inline styles ( shouldnt be using anyway)

        3 ID (#) selector

        2 Class(.)or pseudo-class(:)selector

        1 Element selector (p, div, li, etc.)

        0 Universal selector(*)

    Lowest Priority

for the id, class/Psudo, and Element selectors, if there are multiples of either of those precident goes to the last one in the code.(lowest)

## 32. Inheritence and the universal selector

all the elements in an html body tag can inherit things from the body (mostly for text)

    body { // setting things for the children of the body
        color:#444392;
        font-family: sans-serif;
    }

## 39. Types of boxes

### Block-level

        -elements formatted visually as blocks
        -100% of parent's width
        -Vertically, one after another
        -Box-model applies as showed

### Inline

        -Occupies only content's space
        -Causes no line-breaks
        -Box model is different: heights and widths do not apply
        -Paddings and margins only horizontal(left and right)

### Inline-block

        -Looks like inline from the outside, behaves like block-level on the inside
        -Occupies only content's space
        -Causes no line-breaks
        -Box-model applies as showed

## 40. Absolute Positioning

### Normal Flow

    -Default positioning
    -Elements "in flow"
    -Elements are simply laid out according to their order in the HTML code

    usage
        position: relative

### Absolute Positioning

    -Element is removed from the normal flow: "out of the flow"
    -No impact on surrounding elements, might overlap them
    -We use top, bottom, left or right to offset the element from its relatively positioned container

    usage
        position: absolute

if we set the position of a button to absolute with bottom 50px and right 50px the button will appear at the bottom right of the viewport unless we set its parent to relative. Then it appears at the bottom right of the page instead.

generally we use this method for small things like buttons, not for layouts.

## 41.Pseudo-elements
