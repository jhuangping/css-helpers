# css-helpers

## 初使設定

1. 建立一個 `config.scss` 檔，來管控 Module 預設值

2. 引入 `CssHelpersConfig.scss` : `@import '{ 路徑 }/css-helpers/CssHelpersConfig.scss'`

3. 設定 css-helpers `config.scss` 的值
   
   ```
   // Module Default ///////////////////////////////
   //- Breakpoints
   $useBreakpoints: (
     changeMobile: 1280,
     xl4: 2560,
     xl3: 1920,
     xl2: 1600,
     xl: 1440,
     lg: 1280,
     md: 1024,
     sm: 768,
     xs: 600,
     xs2: 480,
     xs3: 360,
   );
   
   //- Default
   $useWebBase: (
     htmlFontSize: null,
     bodyFontSize: 16,
     bodyLineHeight: 20,
     bodyFontColor: #333
   );
   
   //- Typography Fonts
   $fontDefault: 'Inter', 'Noto Sans TC', Arial, 'Microsoft JhengHei', sans-serif;
   $useFont: (dfk:'DFKai-sb');
   
   //- Color
   
   $useColor: ( 
     'base': map-get($useWebBase, bodyFontColor),
     'hover': #007bff,
     'black': #000,
     'blue': #007bff,
     'indigo': #6610f2,
     'purple': #6f42c1,
     'pink': #e83e8c,
     'red': #dc3545,
     'orange': #fd7e14,
     'yellow': #ffc107,
     'green': #28a745,
     'teal': #20c997,
     'cyan': #17a2b8,
     'white': #fff,
     'gray': #6c757d,
     'gray-dark': #343a40,
     'primary': #007bff,
     'secondary': #6c757d,
     'success': #28a745,
     'info': #17a2b8,
     'warning': #ffc107,
     'danger': #dc3545,
     'light': #f8f9fa,
     'dark': #343a40
   ) !default;
   
   // Layout Module ////////////////////////////////
   //- Wrap (l-wp)
   $useWarp: (
     range: 1024,
     both: 15,
     customName: false
   );
   $useWarpSize: 1680, 1440, 1366, 1140, 1024, 960, 720, 540;
   
   //- Grid (l-gd)
   
   $useGridCount: 2, 3, 4;
   
   // Components Module ////////////////////////////
   // Banner (c-bn)
   
   $bnWidth: 1920;
   
   $bnHeight: 300;
   
   // Utillity Module //////////////////////////////
   // Fonts (u-ff, u-fs, u-fw, u-ta, u-ls, u-lh)
   $useFontBreakpoints: (
     base: false, 
     sm: true, 
     md: true, 
     lg: true, 
     xl: true
   );
   
   // Font Size (u-fs)
   $useFontSizeValue: 12, 14, 16, 18, 20, 25, 30, 35, 40, 45, 50, 55, 60;
   
   // Letter Spacing (u-ls)
   $useLetterSpacingValue: (
     '-1\\.5': -1.5, 
     '-1': -1, 
     '1': 1,
     '1\\.5': 1.5, 
     '2': 2
   );
   
   // Line Height (u-lh)
   
   $useLineHeightValue: (
     0: 0, 
     1: lh(16, 16)
   );
   
   // Display (u-display)
   
   $useDisplayBreakpoints: (
     sm: true, 
     md: true, 
     lg: true, 
     xl: true
   );
   
   // Flex Layout (u-fl, u-jc, u-ai, u-ac, u-as)
   $useFlexBreakpoints: (
     sm: true, 
     md: true, 
     lg: true, 
     xl: true
   );
   
   // Margin (u-m)
   $marginUnit: vw;
   
   $useMarginBreakpoints: (
     sm: true, 
     md: true, 
     lg: true, 
     xl: true
   );
   
   $useMarginValue: 50, 40, 30, 20, 10, auto, clear;
   
   // Padding (u-p)
   $paddingUnit: vw;
   
   $usePaddingBreakpoints: (
     sm: true, 
     md: true, 
     lg: true, 
     xl: true
   );
   
   $usePaddingValue: 50, 40, 30, 20, 10, auto, clear;
   
   // CSS Style ////////////////////////////////////
   //- z-index
   $useZIndex: (
     header: 99,
     gotop: 1,
   );
   ```

4. 再建立 `style.scss` 檔，管控使用的 Module

5. 引入剛剛設定好的`config.scss`  以及  `CssHelpers.scss` : `@import '{ 路徑 }/css-helpers/CssHelpers.scss'`
   
   ```
   // Module Config ////////////////////////////////
   @import 'config.scss' // 剛剛的config
   
   @import '{ path }/css-helpers/CssHelpers'
   ```

6. 設定 css-helpers `style.scss` 的值
   SCSS
   SASS
   
   ```
   // Plugin Style /////////////////////////////////
   // ... Edit Plugin Style
   
   // Module Components ////////////////////////////
   +c-banner()
   +c-button()
   +c-card()
   +c-input()
   +c-textarea()
   +c-form()
   +c-lightbox()
   +c-table() <- 不實用，可刪
   
   // Module Layout ////////////////////////////////
   +l-reset()
   
   +l-base()
   +l-typography()
   +l-main()
   +l-wrap()
   +l-w()
   +l-grid()
   +bootstrap-grid() <- 仿 bootstrap grid v3，可刪
   
   .l-edit
       +l-edit()
       
   // Page Style ///////////////////////////////////
   // ... Edit Page Style
   
   // Module Utility ///////////////////////////////
   +u-image()
   +u-javascript() <- 可刪
   +u-style()
   +u-scroll()
   +u-ff()
   +u-fs()
   +u-ta()
   +u-fc()
   +u-fw()
   +u-bgc()
   +u-ls()
   +u-lh()
   +u-display()
   +u-flex()
   +u-margin()
   +u-padding()
   +u-other()
   ```

## 結構

### Components ( c- )

#### Banner ( c-bn )

#### Button ( c-btn )

#### Card ( c-crd )

#### From ( c-fm )

#### Lightbox ( c-lbx )

### Helpers

#### Breakpoints

#### Compound Css

#### Comput

#### Restore

### Layout ( l- )

#### Reset

#### Default

#### Typography

#### Wrap

#### Grid

### Utility ( u- )

#### Background Color

#### Display

#### Flex layout

#### Fonts

#### Typography

#### Padding

#### Margin

#### Other

### Variable
