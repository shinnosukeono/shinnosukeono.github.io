---
title: Slides
summary: An introduction to using Wowchemy's Slides feature.

authors: [admin]
tags: []
categories: []
date: "2019-02-05T00:00:00Z"

slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: white
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula
---

# Beyond Basic: Advanced simulations in EDEM using the Application Programming and Coupling Interfaces

## May 4th, 2016

## EDEM Academic Advanced Workshop

**J.P. Morrissey**

*Institute for Infrastructure & Environment, School of Engineering*


---

## Presentation Overview
 - Application Programming & Coupling Interfaces Introduction
 - API Examples
  * Edinburgh Cohesion Model 
  * Edinburgh Bonded Model
  * Other applications
 - Multi-Body Dynamics Coupling Examples
  * Jenike Shear Test
  * High Speed Rail
 - Combined API & MBD Usage
  * Caking & Time Consolidation
  * Triaxial testing
 - Concluding Remarks

---
---
# Section 1

## EDEM: Application Programming and Coupling Interfaces

---
# EDEM Application Programming Interface

EDEM simulations can be customized and extended using the EDEM Application Programming Interface (API)​.
With the EDEM API users can write:​

 - Custom contact models to model new particle–particle and particle–geometry interactions​
 - Custom particle body force models to apply new forces and effects to the particles in the simulation​
 - Custom particle factory models to create new methods of particle generation – to define non-standard positions, distributions or flow-rates​
 - Define and work with EDEM Custom Properties, creating custom particle and geometry properties, increasing the scope of user’s custom models​
 - Import 3rd party vector or scalar field data which can be referenced by custom physics models


---
---
## Controls

- Next: `Right Arrow` or `Space`
- Previous: `Left Arrow`
- Start: `Home`
- Finish: `End`
- Overview: `Esc`
- Speaker notes: `S`
- Fullscreen: `F`
- Zoom: `Alt + Click`
- [PDF Export](https://github.com/hakimel/reveal.js#pdf-export): `E`

---

## Code Highlighting

Inline code: `variable`

Code block:
```python
porridge = "blueberry"
if porridge == "blueberry":
    print("Eating...")
```

---

## Math

In-line math: $x + y = z$

Block math:

$$
f\left( x \right) = \;\frac{{2\left( {x + 4} \right)\left( {x - 4} \right)}}{{\left( {x + 4} \right)\left( {x + 1} \right)}}
$$

---

## Fragments

Make content appear incrementally

```
{{%/* fragment */%}} One {{%/* /fragment */%}}
{{%/* fragment */%}} **Two** {{%/* /fragment */%}}
{{%/* fragment */%}} Three {{%/* /fragment */%}}
```

Press `Space` to play!

{{% fragment %}} One {{% /fragment %}}
{{% fragment %}} **Two** {{% /fragment %}}
{{% fragment %}} Three {{% /fragment %}}

---

A fragment can accept two optional parameters:

- `class`: use a custom style (requires definition in custom CSS)
- `weight`: sets the order in which a fragment appears

---

## Speaker Notes

Add speaker notes to your presentation

```markdown
{{%/* speaker_note */%}}
- Only the speaker can read these notes
- Press `S` key to view
{{%/* /speaker_note */%}}
```

Press the `S` key to view the speaker notes!

{{< speaker_note >}}
- Only the speaker can read these notes
- Press `S` key to view
{{< /speaker_note >}}

---

## Themes

- black: Black background, white text, blue links (default)
- white: White background, black text, blue links
- league: Gray background, white text, blue links
- beige: Beige background, dark text, brown links
- sky: Blue background, thin dark text, blue links

---

- night: Black background, thick white text, orange links
- serif: Cappuccino background, gray text, brown links
- simple: White background, black text, blue links
- solarized: Cream-colored background, dark green text, blue links

---

{{< slide background-image="/media/boards.jpg" >}}

## Custom Slide

Customize the slide style and background

```markdown
{{</* slide background-image="/media/boards.jpg" */>}}
{{</* slide background-color="#0000FF" */>}}
{{</* slide class="my-style" */>}}
```

---

## Custom CSS Example

Let's make headers navy colored.

Create `assets/css/reveal_custom.css` with:

```css
.reveal section h1,
.reveal section h2,
.reveal section h3 {
  color: navy;
}
```

---

# Questions?

[Ask](https://github.com/wowchemy/wowchemy-hugo-modules/discussions)

[Documentation](https://wowchemy.com/docs/managing-content/#create-slides)
