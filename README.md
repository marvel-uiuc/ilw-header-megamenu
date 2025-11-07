# ilw-header-megamenu

Links: **[ilw-header-megamenu in Builder](https://builder3.toolkit.illinois.edu/component/ilw-header-megamenu/index.html)** | 
[Illinois Web Theme](https://webtheme.illinois.edu/) | 
[Toolkit Development](https://github.com/web-illinois/toolkit-management)

## Overview

An Illinois Mega Menu utilizes the standard design of the header menu, including the ability to have a link and toggle dropdown or just a static label with toggle dropdown. The difference will be the dropdown takes up the full-width of the container maxing out at 1240px, exceeding the length of the main nav bar items.

Each dropdown section has a maximum of 4 columns, evenly spaced with a diving bar between each. Within each column you can perscribe a lists of links, one level of nested list links, decorative images or buttons. By default each column has a maximum of 5 list items. If you choose to make the columns distinct you can have more items, but if all of the items apply to the section in no particular order they will be split into 5 equal columns. See about and admissions dropdown in this example: [illinois.edu](https://illinois.edu/)

The mega menu is not suited for more than 1 layer of nested lists, if you require more, use a flyout menu instead.

## Code Examples

```html
<ilw-header-megamenu slot="navigation">
    <ul>
      <li>
      <a class="mega-menu__link" href="https://illinois.edu/about/">
      About</a>
      <button aria-haspopup="true" aria-expanded="true" aria-controls="About-menu" aria-label="Toggle About submenu"></button>
        <ilw-header-megamenu-section>
          <span slot="label">Start Here</span>
          <ul>
            <li><a href="/getting_started/index.html">Getting Started</a></li>
            <li><a href="/create_page/index.html">Create a Page</a></li>
            <li><a href="/upgrade/index.html">Upgrade from V2</a></li>
          </ul>
        </ilw-header-megamenu-section>
      </li>
      <li>
        <ilw-header-megamenu-section>
          <span slot="label">Information</span>
          <ul>
            <li><a href="/philosophy/index.html">Philosophy</a></li>
            <li><a href="/links/index.html">Helpful Links</a></li>
            <li><a href="/github/index.html">Organization and Github</a></li>
          </ul>
        </ilw-header-megamenu-section>
      </li>
      <li>
        <a href="/demo/index.html">Demo Pages</a>
      </li>
      <li>
        <a href="/components_toc/index.html">Components</a>
      </li>
      <li>
        <a href="/preview/index.html">Component Preview</a>
      </li>
    </ul>
</ilw-header-megamenu>
```

## Accessibility Notes and Use

Note from Keith: 
   - Navigation / Menus are unique in that most screen reader users will only expect linked items to exist inside of this element role. This means that any headings or static text should be avoided since they will likely be missed by this audience.

### Keyboard navigation
- While all dropdowns are closed: Use `Tab/Shift + Tab` or `left/right arrow keys` move the user across the top level navigation bar.
- Open a dropdown: Focus on the toggle button and press `enter` or `space`.
- Navigate an open dropdown: `Tab/Shift + Tab` or `down/up arrow keys` will go down/up the list. 
- Close an open dropdown: Press `escape` to close and return focus to the corresponding toggle button. `Left/right arrow keys` will close the dropdown and go to the next item in the top level navigation bar.


### ARIA
- Each toggle button will get the attributes: `aria-haspopup="true"`, `aria-expanded="true"`, `aria-controls="parent-name-menu"` and `aria-label="Toggle parent-name submenu`. The SVG will get `aria-hidden="true"`
- Each section will get a unique id and label, example: `id="parent-name-menu"` and `aria-label="About submenu"`

## External References

See [ilw-header documentation](https://github.com/web-illinois/ilw-header-menu)
