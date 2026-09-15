# ✨ Background Animation Project

An interactive, grid-based visual effect built with pure HTML, CSS, and JavaScript. As the user hovers over the viewport, dynamically generated tiles expand and reveal portions of a fixed background image with smooth fade transitions, creating a dynamic reveal and ripple impression.

---

## Features

- Interactive mouse-driven hover animation
- Dynamic DOM generation creating an immersive full-screen tile grid
- Fixed background attachment giving a seamless reveal across separate grid elements
- Instant hover response with gradual fade-out transition
- Zero dependencies or external libraries
- Runs directly in any modern web browser

---

## Tech Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Base document structure and container layout |
| CSS3 | Flexbox grid, pseudo-elements, fixed background clipping, and transitions |
| JavaScript (ES6) | Dynamic element generation and DOM injection |

---

## Project Structure

```
Background-Animation-Project-HTML-CSS-JAVASCRIPT-/
├── index.html       
├── style.css        
└── index.js         
```

---

## How It Works

1. **Grid Generation (`index.js`)**: A simple JavaScript loop instantiates 2,000 `<span>` elements and appends them into the `.container` wrapper.
2. **Fixed Background Illusion (`style.css`)**: Each `<span>` has a `::before` pseudo-element referencing an image with `background-attachment: fixed`. Because the background is locked to the viewport, all tiles reveal coherent parts of the same image.
3. **Transition Dynamics**:
   - **Default State**: Pseudo-elements have an opacity of `0` and a long `20s` transition, creating a slow fade-out trail when cursor leaves.
   - **Hover State (`:hover::before`)**: Transition resets to `0s`, opacity snaps to `1`, and tile dimensions expand instantly to reveal the image under the cursor.

---

## Getting Started

No build steps, installations, or local servers are required.

### 1. Clone the repository

```bash
git clone https://github.com/Kumar44developer/Background-Animation-Project-HTML-CSS-JAVASCRIPT-.git
```

### 2. Run the project

Open `index.html` directly in your web browser, or launch it with any local server extension (such as VS Code Live Server).

---

## Customization

- **Change Background Image**: Update the image URL inside `style.css` on line 29:
  ```css
  background: url(YOUR_IMAGE_URL_HERE);
  ```
- **Adjust Grid Density**: Modify the loop counter in `index.js` to increase or decrease tile density:
  ```javascript
  for(let i = 1; i < 2000; i++)
  ```
- **Change Trail Duration**: Alter the default `transition` duration in `.container span::before` in `style.css` to lengthen or shorten the fade-out effect.

---

## Author

**Kumar44developer** — [GitHub Profile](https://github.com/Kumar44developer)
