# CSS-Practice

Project For Modern CSS Practice

# What I Learned(Blog Post)

What is clip path in CSS

1. What box-sizing
   making box-sizing=border-box change to box model so that border and padding not get added.
   clip-path
   we defines some quardinate of polygon

# Day-2

1. Absolute position
2. Easiest way to center any element.
3. How to implement CSS animation
4. If You want some height width, padding etc then make inline element display block.
5. Transform is very important property.

# Day 3

1. After Sudo Element
2. content css property
3. How to send after content behind - use position
4. z-index - it defines position of element if they are one and top of other
5. animation-fill-mode
6. Three Pillar of writing good website

- Responsive design
- Maintainable and Scalable code(clean, easy to understand, growth, reusable, how to organise files, how name classes, how to structure HTML)
- Performance

# Day 4

1. How Browser render HTML, CSS?

- First Browser load the HTML and then parse it.
- fter that browser builds DOM(web document is html tag tree).
- Now browser loads CSS and Parse it. While parsing CSS browser resolves conflicting CSS declaration(cascade) and process final values(all value for margin etc at the end it will be in pixel).

2. After this final CSS is also stored in form of tree (CSSOM).
3. Now using HTML DOM and CSSOM browser creates a rendered tree.
4. Then browser uses Visual formatting model to render ther page on screen.

## Cascade

Cascade is the process of combining different CSS stylesheets and resolving the conflicts between different CSS rules and declaration, when more than one rule applies to a certain element.
There are some default declaration thats called user agent CSS.

Importance-> Specificity-> Source Order

### Importance(Weight)

- User !importance declaration
- Author !importance declaration
- Author declarations
- User Declarations
- Default Browser declarations
  If same importance then??

### Specificity

- Inline style
- IDs
- Classes pseudo classes attribute
- Elements, pseudo elements
  Calculating specificity (inline, ids, classes, elements, pseudo elements) --> all are counts

If all have same specificity??

### Order of Declaration

- If all selector have same specifity then last declaration is applied.

## CSS Parsing: Value Processing

- Each CSS property has initial value.
- Each CSS property need to have a value.
- Default value of font-size is 16px.
- Default padding is 0px.
- actual value stored during rendering page
- Some property that is related to text inherit computed value of root
  Declared Value(Author Declaration)
  Cascaded Value(After cascade)
  Specified Value(defaulting if there is no cascaded value)
  computed value: converting relative value to absolute
  Used value(Final calculation based on layout)
  Actual Value(Browser and device restriction)

### Value unit(rem)

- rem is always uses root for reference.
- em uses parent component for reference.
- 10vh: 10% of viewport height
- 10vw: 10% of viewport width

### Inheritance

- Each and every CSS property must have a value if not declared then browser will assign default value.
- First browser will check if property has cascaded value or not? if yes then it will assign that value else it will check if this property can be inherited? if yes then it will assign computed value of parent element else initial value.
- property related to text get inherited.
- margin padding can not be inherited.
- computed value get inherited not declared value.
- Inheritance of a property will work if no one(either browser or developer) declared the value.
- inherit keyword forces to inheritence certain propert.
- initial keywork used to resets a property to it initial value.

# Day 5

1. Why to change value from absolute to relative?
   Change absolute value to rem so that you can modify all value by modfying on value.
2. It is good practice to use rem.
3. Always use relative value.
4. Use .5 instead of 0.5 for good practice.
5. Using px is not good practice.
6. rem is not supported in IE below 9 version.

## The Visual formatting Model

Algorithm that calculates boxes and determines the layout of these boxes, for each element in the render tree, in order to determine the final layout of the page.
Dimension of Boxes 
Box type: inline, block, and inline-block
Positioning scheme: floats or positioning
Stacking contexts
Other elements in render tree.
View port size, dimention of images, etc.

### How Box Model works?
- First- Content: Text, images, etc.
- Padding: Transparent area around inside the box.
- Border
- Margin: space between box
- Fill Area: area that get filled with bg-color or bg-image.
#### Height and Width of box mode
If height or width is not defined then Visual formatting Model will uses content to define height. 