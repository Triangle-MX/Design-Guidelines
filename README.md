# Triangle Design Guidelines

## Design Values
<ul>
    <li>Colorful and Playful</li>
    <li>Simple</li>
    <li>Interactive</li>
</ul>

## Logo
Three versions of the logo currently exist:

<ul>
    <li>
        <strong>Main/Yellow Version</strong>
        <p>Can be used over both white and black backgrounds.</p>
    </li>
    <li>
        <strong>Black Version</strong>
        <p>Can be used over white and light grey backgrounds.</p>
    </li>
    <li>
        <strong>White Version</strong>
        <p>Can be used over yellow, black, blue, and other colored backgrounds backgrounds.</p>
    </li>
</ul>

Find the related assets <a href="assets/logo/">here</a>.

### The Triangle Icon
The **Triangle** (letter *A*), may be used as an icon or favicon. Find the related assets <a href="assets/logo/icon/">here</a>.

### Logo Variations
The logo was designed as a **logo system**, which means it can be modified to suit certain topic, for example, Christmas. Find the related assets <a href="assets/logo/variations/">here</a>.

## Colors
### Color Scheme
The Triangle color scheme consists in mainly 5 colors:

<ul>
    <li>
        <strong style="background-color: #FFB61E; color: #ffffff; padding:1px;">Bungee (#FFB61E)</strong>
        <p>Primary color of the brand. Used as main color in the website (buttons, accents).</p>
    </li>
    <li>
        <strong style="background-color: #1b1b1b; color: #ffffff; padding:1px;">Dark Night (#1B1B1B)</strong>
        <p>Secondary color of the brand. Used as the hover background in the website's buttons and other interactive components.</p>
    </li>
    <li>
        <strong style="background-color: #EEEEEE; color: #1b1b1b; padding:1px;">Monotonous Grey (#EEEEEE)</strong>
        <p>Used for social media and to have an alternative to White.</p>
    </li>
    <li>
        <strong style="background-color: #1E81FF; color: #ffffff; padding:1px;">Bluejay (#1E81FF)</strong>
        <p>Accent/Selection color of the brand. Main color for Spark.</p>
    </li>
    <li>
        <strong style="background-color: #ffffff; color: #1b1b1b; padding:1px;">White Night (#FFFFFF)</strong>
        <p>White. Used in whitespace.</p>
    </li>
</ul>

### Other Colors
If you need any other color (i.e. red for an alert), you can refer to <a target="_blank" "_" href="https://flatuicolors.com">Flat UI Colors</a>.

## Typography
In Triangle we use two main fonts:

<ul>
    <li><strong>Montserrat</strong> for headings and emphasis.</li>
    <li><strong>Lato</strong> for normal text.</li>
</ul>


## SASS Components

### Variables
To develop faster we have a series of basic SASS variables for things like animations, transitions, colors, typography, shadows, borders, and more...
```sass
// Color Variables
$yellow: #FFB61E
$black: #1B1B1B
$white: #FFFFFF
$grey: #EEEEEE
$blue: #1E81FF

// Typography Variables
$anton: "Anton", "Helvetica Neue", sans-serif
$montserrat: "Montserrat", "Helvetica Neue", sans-serif
$lato: "Lato", "Helvetica Neue", sans-serif
$normal-size: 18px
$mobile-size: 16px
$big-size: 20px

// Transition Variable
$transition: .2s cubic-bezier(1,.55,0,.87)

// Shadow Variables
$box-shadow: 5px 5px 100px 0px rgba(27,27,27,0.16)
$box-shadow2: 7px 7px 100px 0px rgba(27,27,27,0.16)

// Border Variables
$border-radius: 5px
```

### Components
This is a list of pre-built SASS components for Triangle-related sites:

<ul>
    <li><a href="assets/components/sass/parsec.sass">Parsec</a> (Boilerplates and Components for faster development, built by us).</li>
    <li><a href="assets/components/buttons.sass">Buttons</a></li>
    <li><a href="assets/components/form.sass">Forms</a></li>
</ul>

## Animations and Transitions
We have a fixed transition for things like hovers (for both buttons and links), transformations, etcetera... It is:
```sass
// Variable
$transition: .2s cubic-bezier(1,.55,0,.87)

// Usage
.class, #id, element    
    transition: $transition
```

As you may note, we use `cubic-bezier(1,.55,0,.87)` for our animations and transitions, but we also accept the use of the `ease-in` curve. This means that you should use either the customized beizer curve or the ease-in one in non-web animations (i.e. videos).

## Shadows
We mainly use flat design, but for things like modals and some containers (see <a href="https://triangle.mx/#desarrollo" target="_blank" "_") we do use shadows.

In websites, we use
```sass
// For medium-sized elements    
$box-shadow: 5px 5px 100px 0px rgba(27,27,27,0.16)

// For large elements
$box-shadow2: 7px 7px 100px 0px rgba(27,27,27,0.16)
```

## Hover and Focus
We use hovers in websites for two things: demonstrate interactivity (buttons) and emphasize content (sections).

In elements that can be interacted with, we normally only change the background for the element (i.e. buttons), but in some cases we use `transform: scale(1.1)` or `transform: scale(1.05)` and `box-shadow: $box-shadow` or `box-shadow: $box-shadow2` (i.e. cards, Spark Button).

To emphasize content (like text) we only use the `transform` and the `box-shadow` properties.

In links, we eliminate the underlining, always. Instead, to indicate the element is a link, we utilize color (i.e. blue) and typography (i.e. bold). This is how we commonly style links:

```sass
a
    text-decoration: none
    color: $blue // Sometimes we use $yellow instead
    transition: $transition

    &:hover, &:active, &:visited
        color: $black
        text-decoration: none
```
