# A quick CSS3 Grid Layout 

**1. Basic Grid Layout**
A very simple 12 column grid layout.

```css
.basic-grid {
  display: grid;
  gap: 1rem;

  /* grid-template-columns: repeat(12, 1fr); */

  /* better sizing, but overflow */
  /* grid-template-columns: repeat(12, minmax(240px, 1fr)); */

  /* better sizing, and no overflows */
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
}
```

### Output :

<img src="../Grid&#32;Project/display/basic-grid.png">

<hr>

**2. Photo Gallery Grid Layout**
```css
.photo-grid {
  display: grid;
  gap: 1rem;

  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  grid-auto-rows: 240px;
}
```

### Output :
<img src="../Grid&#32;Project/display/photo_gallery.png">

<hr>

**3. Animated Grid Layout**

```css
.animated-grid {
  height: 85vh;

  display: grid;
  gap: 1rem;

  /* Explicit grid */
  grid-template-areas:
    "a b c d"
    "l 🌟 🌟 e"
    "k 🌟 🌟 f"
    "j i h g";

  grid-template-rows: repeat(4, 25%);
  grid-template-columns: 240px auto auto 240px;

  --stagger-delay: 100ms;
}

```

### Output :
<img src="../Grid&#32;Project/display/animated_grid.png">
