# React Side Menu
Multi level side menu component

![react-side-menu](https://cloud.githubusercontent.com/assets/4214509/19636936/7482a036-99f6-11e6-8429-d6efb75ef6ce.gif)

# Install

   npm install --save react-side-menu
   
# Usage

Define menu object:

    const menu = [
      {
        key: 'accounts', name: 'Accounts', icon: 'fa-home', link: '#accounts',
        childs: [
          {
            key: 'siliconstraits', name: 'Silicon Straits', link: '#siliconstraits',
            childs: [
              {
                key: 'spacewalker', name: 'Space Walker', link: '#spacewalker',
                childs: [
                  { key: 'internal', name: 'Internal Team', link: '#internal' },
                  { key: 'external', name: 'External Team', link: '#external' },
                ]
              },
              { key: 'minion', name: 'Minion', link: '#minion' },
              { key: 'tinker', name: 'Tinker', link: '#tinker' },
            ],
          },
          {
            key: 'microsoft', name: 'Microsoft', link: '#microsoft',
            childs: [
              { key: 'bill', name: 'Bill', link: '#bill' },
              { key: 'gates', name: 'Gates', link: '#gates' },
            ],
          },
          {
            key: 'google', name: 'Google', link: '#google',
            childs: [
              { key: 'chrome', name: 'Chrome', link: '#chrome' },
              { key: 'gmail', name: 'Gmail', link: '#gmail' },
            ],
          },
          {
            key: 'life', name: 'Life', link: '#life',
            childs: [
              { key: 'giang', name: 'Giang', link: '#giang' },
              { key: 'code', name: 'Code', link: '#code' },
            ],
          },
        ]
      },
      {
        key: 'setting', name: 'Setting', link: '#setting', icon: 'fa-gear',
      }
    ];

In your `render()`:

        <Menu menu={menu} activeMenu={'siliconstraits'} />

# Disclaimer

This component depends on global Font Awesome icon pack to renders some icons.

# Options
## `<Menu>` Component:
- `menu` - [`MenuObject`](#menu-object): describe menu structure & content.
- `activeMenu` - `String`: unique identity of the active menu, this is used to decide what menu to highlight.

## Menu Object:
- `key` - `String`: Unique identity of a menu item
- `name` - `String`: Text to display
- `link` - `String` - (optional): This will be put in `href` of the `<a>` tag when render the menu item, if this is empty the link will be rendered with `<a href="#">`.
- `icon` - `String` - (optional): font awesome class icon, will be append to class name of `<i class="fa ">`.
- `childs` - `Array[MenuObject]`: child menus.

# Styling
