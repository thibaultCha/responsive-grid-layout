# Responsive Grid Layout

A responsive grid layout in [Less](http://lesscss.org), trying to mimic [Semantic](http://semantic.gs/) as an experiment.

[JSFiddle demo](http://jsfiddle.net/thibaultCha/kKBZT/).

### Usage

1. Import `grid.less`.

2. ***Optionally*** override those varibles in `grid.less`:

```
@nbcols: 12; // how many columns in a row
@colwidth: 40; // width of a column
@gutterwidth: 10; // width of a column offset
```

3. ***Optionally*** run the loop in one or several media query(ies) to create a responsive layout:

```
@media (min-width:981px) {
  .loop(@nbcols, ''); // will create classes col_width_X
}

@media (max-width:980px) {
  .loop(@nbcols, 'm_'); // will create classes m_col_width_X specific for thin displays
}
```

In your HTML, you can now use the created classes:

```html
<div class="row">
  <div class="col_width_6 m_col_width_12"></div>
  <div class="col_width_6 m_col_width_6 m_col_offset_by_6"></div>
</div>
```

### License

Copyright (C) 2013 by Thibault Charbonnier.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

