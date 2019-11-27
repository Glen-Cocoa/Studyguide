# HTML

HTML is _HyperText Markup Language_, used for conveying the content that is present in a web page. It consists of a [tree](https://en.wikipedia.org/wiki/Tree_(data_structure)) structure of _parent_ and _child_ __nodes__. 

![HTML Tree](https://www.w3schools.com/whatis/img_htmltree.gif)
image taken from W3 Schools [html dom](https://www.w3schools.com/whatis/whatis_htmldom.asp) page


## Parent/Child Relationship

In the above example image, __Document__ is the _parent_ of it's _child_ element`Root element:<html>`

The vocabulary Parent/Child simply refers to the relationship of nodes in a tree structure. Each block, or leaf, is referred to as a `Node`. Nodes above an element are referred to as it's _parent_. nodes below are it's _children_. 

## Element Attributes
An HTML Node can also be referred to as an _element_. An HTML element can be represented by the syntax:

```
<div> Some Text </div>
```

When manipulating HTML, we want to be able to specify which HTML Element we want to target. This is most easily done with the _attribute_ _class_ and _id_.

### Class
You can assign a class to an element with the syntax:
```
<div class='someClass'> My Text Here</div>
```
Elements can have multiple classes separated by spaces:
```
<div class='classOne classTwo'> Foobar </div>
```

### ID

ID is a unique identifier assigned to an element. You should not assign ID to more than one element. It is assigned with the syntax:
```
<div id="someID"> Hello World </div>
```