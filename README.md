# ilw-header-megamenu

Links: **[ilw-header-megamenu in Builder](https://builder3.toolkit.illinois.edu/component/ilw-header-megamenu/index.html)** | 
[Illinois Web Theme](https://webtheme.illinois.edu/) | 
[Toolkit Development](https://github.com/web-illinois/toolkit-management)

## Overview

An Illinois Mega Menu has a maximum of 4 columns. In each column you can perscribe a lists of links, one level of nested list links, decorative images and buttons.

The mega menu is not suited for more than 1 layer of nested lists, if you require more, use a flyout menu instead.

Each column has a maximum of 5 list items. If you choose to make the columns distinct you can have more items, but if all of the items apply to the section in no particular order they will be split into 5 equal columns.

## Code Examples

```html
<ilw-header-megamenu slot="navigation">
    <ul>
      <li>
      <a class="mega-menu__link" href="https://illinois.edu/about/">
      About</a>
      <button aria-haspopup="true" aria-expanded="true" aria-controls="About-menu" aria-label="Toggle About submenu"></button> 
        <ilw-mega-menu-section role="region" >
          <span slot="label">Start Here</span>
          <ul>
            <li><a href="/getting_started/index.html">Getting Started</a></li>
            <li><a href="/create_page/index.html">Create a Page</a></li>
            <li><a href="/upgrade/index.html">Upgrade from V2</a></li>
          </ul>
        </ilw-mega-menu-section>
      </li>
      <li>
        <ilw-mega-menu-section role="region">
          <span slot="label">Information</span>
          <ul>
            <li><a href="/philosophy/index.html">Philosophy</a></li>
            <li><a href="/links/index.html">Helpful Links</a></li>
            <li><a href="/github/index.html">Organization and Github</a></li>
          </ul>
        </ilw-mega-menu-section>
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

Menu's are unique in that most screen reader users will only expect linked items to exist inside of a menu. This means that any headings or static text should be avoided.

## External References
