---
sidebar_position: 2
---

# Creating a System Theme


1. Remember to put your github url, and if you are basing the theme off another color scheme note it below or just write `custom`
```js {1,2,3,5-17} title="src/lib/themes/custom.ts"
// https://github.com/diced/
// custom
import createTheme from '.';

export default createTheme({
  type: 'light',
  primary: '#FFF',
  secondary: '#FFF',
  error: '#FFF',
  warning: '#FFF',
  info: '#FFF',
  border: '#FFF',
  background: {
    main: '#FFF',
    paper: '#FFF'
  }
})
```
2. Add your theme to `src/components/Theming.tsx`
```js {8,18,29} title="src/lib/themes/index.ts"
import dark_blue from 'lib/themes/dark_blue';
import dark from 'lib/themes/dark';
import ayu_dark from 'lib/themes/ayu_dark';
import ayu_mirage from 'lib/themes/ayu_mirage';
import ayu_light from 'lib/themes/ayu_light';
import nord from 'lib/themes/nord';
import polar from 'lib/themes/polar';
import white_af from 'lib/themes/white_af'; // the theme from above

export const themes = {
  'dark_blue': dark_blue,
  'dark': dark,
  'ayu_dark': ayu_dark,
  'ayu_mirage': ayu_mirage,
  'ayu_light': ayu_light,
  'nord': nord,
  'polar': polar,
  'white_af': white_af // add your theme here
};

export const friendlyThemeName = {
  'dark_blue': 'Dark Blue',
  'dark': 'Very Dark',
  'ayu_dark': 'Ayu Dark',
  'ayu_mirage': 'Ayu Mirage',
  'ayu_light': 'Ayu Light',
  'nord': 'Nord',
  'polar': 'Polar',
  'white_af': 'White AF!' // create a formal/friendly name for your theme so it wont appear as "white_af"
};
```
3. And that's it. Make sure to test your theme before making a PR and make sure it looks good, or your PR will be closed.