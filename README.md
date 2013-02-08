after-font-awesome
==================

Font Awesome with LESS mix-in and double-icon capabilities

## Example: Standard Usage (class still supported)
    <div class="my-menu-module">
      <ul>
        <li><a class="icon-book" href="...">Item 1</a></li>
        <li><a class="icon-list-ol" href="...">Item 2</a></li>
        <li><a class="icon-calendar" href="...">Item 3</a></li>
      </ul>
    </div>

## Example: Two Icons (class + mix-in)

    <div class="my-menu-module">
      <ul>
        <li><a class="icon-book" href="...">Item 1</a></li>
        <li><a class="icon-list-ol" href="...">Item 2</a></li>
        <li><a class="icon-calendar" href="...">Item 3</a></li>
      </ul>
    </div>

    // explicitly specify an :after font-awesome icon
    .my-menu-module {
      a {
        position: relative;
        .fontAwesome;
        .icon-chevron-right(after);
        &:before{
          float: left;
        }
        &:after {
          float: right;
        }
      }
    }

## Example: Two Icons (two mix-ins)

    <div class="my-menu-module">
      <ul>
        <li><a href="...">Item 1</a></li>
        <li><a href="...">Item 2</a></li>
        <li><a href="...">Item 3</a></li>
      </ul>
    </div>

    // explicitly specify both :before and :after font-awesome icons
    .my-menu-module {
      a {
        position: relative;
        .fontAwesome;
        .icon-chevron-right(after);
        .icon-book(before);
        &:before{
          float: left;
        }
        &:after {
          float: right;
        }
      }
    }
