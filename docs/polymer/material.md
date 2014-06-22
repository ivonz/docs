---
layout: default
type: core
navgroup: docs
shortname: Docs
title: Material design with Polymer
subtitle: Guide
---

<!-- <link rel="import" href="/elements/paper-demo-elements.html"> -->

<style shim-shadowdom>
  .icondemo core-icon {
    margin: 20px;
  }
  .demo-table paper-slider,paper-progress,paper-input {
    width: 150px;
  }

  paper-button.purpleRipple::shadow #ripple {
    color: #9f499b;
  }
  .demo-card {
    width: 100px;
    height: 100px;
    background: #eee;
    text-align: center;
    margin: 20px;
    padding: 10px 5px;
  }
  .demo-card p {
    padding: 5px 0px;
  }
</style>

{% include toc.html %}

Material design is a unified system of visual, motion, and interaction design
that adapts across different devices. Material design is inspired by tactile
materials, such as paper and ink. Material surfaces interact in a shared
space. Surfaces can have elevation (z-height) and cast shadows on other
surfaces to convey relationships.

{{site.project_title}}'s [paper elements collection](/docs/elements/paper-elements.html)
implements material design for the web. The [{{site.project_title}} core elements
collection](/docs/elements/core-elements.html) provides a number of unthemed
elements that you can use to achieve material design app layouts, transitions,
and scrolling effects.

For more detail on the material design philosophy and guidelines, see the
[Material design specification]().

For a sample of the material design patterns in use, see the <a href="/apps/topeka/" target="_blank">Topeka sample app</a>.

For quick visual demos of many of the paper elements, see the <a href="/components/paper-elements/demo.html" target="_blank">Paper elements sampler</a>.

## Application layout

The {{site.project_title}} core elements set includes several elements for application layout,
including creating toolbars, app bars, tabs, and side nav consistent with the
material design guidelines.

See [Layout elements](/docs/polymer/layout-elements.html) for information on
using these elements.

To work well with the {{site.project_title}} layout elements, you should make sure other
parts of your app follow the same metrics described in the [material design
spec](), such as:

* Baseline grids
* Keylines
* Touch target size

## Icons

Material design uses icons extensively. {{site.project_title}} provides access
to a large variety of scalable, tintable  SVG icons using the `<core-icon>`
element and its associated icon sets. Using `<core-icon>` can be as simple as:

    <link rel="import" href="/components/core-icons/core-icons.html">
    <core-icon icon="info"></core-icon>

`core-icons.html` is a utility import that includes the `<core-icon>` element
and the default icon set, which  includes over 150 common icons. Here are a
few examples:

<div class="icondemo" layout horizontal>
  <core-icon icon="send"></core-icon>
  <core-icon icon="credit-card"></core-icon>
  <core-icon icon="visibility" style="fill: #5168ff;"></core-icon>
  <core-icon icon="favorite" style="fill: #d61a7f;"></core-icon>
  <core-icon icon="polymer" style="fill: #9f499b;"></core-icon>
  <core-icon icon="save"></core-icon>
  <core-icon icon="language"></core-icon>
</div>
<div class="icondemo" layout horizontal>
</div>

For details on using `<core-icon>` and its relatives, see 
[Using core icons](/docs/polymer/icons.html).

## Material controls

The paper elements collection includes a number of material-themed controls
for all common areas of your application. The following table shows the common 
controls.

<table class="demo-table">
  <thead>
    <tr>
      <th>Control</th>
      <th>Example</th>
      <!-- <th>Info</th> -->
    </tr>
  </thead>
  <tr>
    <td>Button<br>
    <a href="/docs/elements/paper-elements.html#paper-button"><code>&lt;paper-button&gt;</code></a></td>
    <td><paper-button label="play" raisedButton></paper-button></td>
    <td><a href="/components/paper-elements/demo.html#paper-button"><core-icon icon="arrow-forward" size="16"></core-icon> More examples</a></td>
  </tr>
  <tr>
    <td>Checkbox<br>
    <a href="/docs/elements/paper-elements.html#paper-checkbox"><code>&lt;paper-checkbox&gt;</code></a></td>
    <td><paper-checkbox label="Enable"></paper-checkbox></td>
  </tr>
  <tr>
    <td>Toggle button<br>
    <a href="/docs/elements/paper-elements.html#paper-toggle-button"><code>&lt;paper-toggle-button&gt;</code></a></td>
    <td><paper-toggle-button label="play"></paper-toggle-button></td>
  </tr>
  <tr>
    <td>Icon button<br>
    <a href="/docs/elements/paper-elements.html#paper-icon-button"><code>&lt;paper-icon-button&gt;</code></a></td>
    <td><paper-icon-button icon="search"></paper-icon-button><paper-icon-button icon="favorite"></paper-icon-button></td>
    <td><a href="/components/paper-elements/demo.html#paper-icon-button"><core-icon icon="arrow-forward" size="16"></core-icon> More examples</a></td>
  </tr>
  <tr>
    <td>Floating action button<br>
    <a href="/docs/elements/paper-elements.html#paper-fab"><code>&lt;paper-fab&gt;</code></a></td>
    <td><paper-fab icon="add"></paper-fab></td>
  </tr>
  <tr>
    <td>Radio buttons<br>
    <a href="/docs/elements/paper-elements.html#paper-radio-group"><code>&lt;paper-radio-group&gt;</code></a><br>
    <a href="/docs/elements/paper-elements.html#paper-radio-button"><code>&lt;paper-radio-button&gt;</code></a></td>
    <td>
      <paper-radio-group selected="0">
        <paper-radio-button label="Now"></paper-radio-button><br>
        <paper-radio-button label="Later"></paper-radio-button>
      </paper-radio-group></td>
  </tr>
  <tr>
    <td>Slider<br>
    <a href="/docs/elements/paper-elements.html#paper-slider"><code>&lt;paper-slider&gt;</code></a></td>
    <td><paper-slider pin></paper-slider></td>
  </tr>
  <tr>
    <td>Progress bar<br>
    <a href="/docs/elements/paper-elements.html#paper-progress"><code>&lt;paper-progress&gt;</code></a></td>
    <td><paper-progress value="30"></paper-progress></td>
  </tr>
  <tr>
    <td>Input<br>
    <a href="/docs/elements/paper-elements.html#paper-input"><code>&lt;paper-input&gt;</code></a></td>
    <td><paper-input floatingLabel label="First name"></paper-input></td>
    <td><a href="/components/paper-elements/demo.html#paper-icon-input"><core-icon icon="arrow-forward" size="16"></core-icon> More examples</a>
    </td>
  </tr>
</table>


## Dialogs, snackbars, and toasts

Dialogs, snackbars and toasts all appear as a separate sheet, overlaying the
background. The paper element collection includes two elements.

-   A _dialog_ (`<paper-dialog>`) is a modal window that can include a title,
    text, action buttons, and other controls.

-   A _snackbar_ or _toast_ (`<paper-toast>`) is a small, transient popup that
    includes a message and optionally a _single_ action (such as "undo").

### Dialogs

Use the `<paper-dialog>` element to create a dialog. Set a title on a dialog
using the `heading` published property.

You can use any kind of children inside the dialog. For action buttons, add
the `dismissive` or `affirmative` attributes to place the controls (typically
buttons) at the bottom of the dialog:

-   `dismissive` actions, like **Cancel**, close the dialog and return to the
    previous screen without making changes. They're displayed on the left.

-   `affirmative` actions, like **OK** or **Save** continue a process or
    confirm a decision. They're displayed on the right.

The following example creates a dialog with two buttons:

    <paper-dialog id="dialog" heading="Launch?"
                  transition="paper-dialog-transition-bottom">
      <p>This app would like to launch a small, unmanned vehicle
         into space.</p>
      <paper-button label="Cancel" dismissive></paper-button>
      <paper-button label="OK" affirmative default></paper-button>
    </paper-dialog>

<paper-dialog id="dialog" heading="Launch?" transition="paper-dialog-transition-bottom">
<p>This app would like to launch a small, unmanned vehicle into space.</p>

<paper-button label="Cancel" dismissive></paper-button>
<paper-button label="OK" affirmative default></paper-button>

</paper-dialog>

<paper-button id="dialog-button" label="Show me the dialog" raisedButton></paper-button>

In this example, the default button has a `default` attribute. The dialog
doesn't apply any special treatment for a default option; you can style it
differently using CSS.

Dialogs are hidden by default. Call the dialog's `toggle` method to show or
hide it.

<a href="/components/paper-elements/demo.html#paper-dialog">
<core-icon icon="arrow-forward" size="16"></core-icon> More examples</a>

### Snackbars & toasts

A `<paper-toast>` element appears at the bottom of the screen or on the 
lower-left on mobile. Use the `text` attribute to specify the text to display.

    <paper-toast id="toast" text="Your draft has been discarded."></paper-toast>

<paper-toast id="toast" text="Your draft has been discarded."></paper-toast>

<paper-button id="toast-button" label="Show me the snackbar" raisedButton></paper-button>

Like a dialog, a `<paper-toast>` is hidden by default. Call the element's
`open` method to display it. The toast disappears after a timeout, or can be
dismissed by swiping.

<a href="/components/paper-elements/demo.html#paper-toast">
<core-icon icon="arrow-forward" size="16"></core-icon> More examples</a>

## Material effects

When designing your own components or using generic HTML elements such as
`<div>`s, you can add material design effects using the `<paper-ripple>` and
`<paper-shadow>` elements.

### Touch ripple effect

Material responds to input events with an touch ripple effect: an animation
that moves out radially from the origin of the event. These effects are built
into the 
[paper elements collection](/docs/elements/paper-elements.html):

<paper-button class="purpleRipple" 
  label="Show me the ripple" raisedButton></paper-button>

When working with other elements, you can use the `<paper-ripple>` element to
create a touch ripple effect.

To use `<paper-ripple>`, declare a `<paper-ripple>` element as a child of the
element you want to add the effect to:

    <div style="position: relative;">
      <paper-ripple fit></paper-ripple>
    </div>

Touch the cards below to see ripple effects.

<div layout horizontal>
<div class="demo-card" style="position: relative;">
  <p>Default ripple</p>
  <paper-ripple fit></paper-ripple>
</div>
<div class="demo-card" style="position: relative;">
  <p>Colored ripple</p>
  <paper-ripple fit style="color: red;"></paper-ripple>
</div>
<div class="demo-card" style="position: relative;">
  <p>Circular ripple</p>
  <paper-ripple fit class="circle"></paper-ripple>
</div>
</div>


The `<paper-ripple>` should be `position: absolute` and sized to fit the
parent element. In  this example, the `fit` layout attribute is used to
position the ripple appropriately.  (See 
[layout attributes](/docs/polymer/layout-attrs.html) for information on `fit` 
and other layout attributes.)

You can clip the ripple to a circle by adding the `circle` class to the
ripple's classlist.

You can set the color of the ripple using the `color` CSS property. 

    paper-ripple {
      color: red;
    }

When using a paper element, check the element API doc to find the CSS selector 
to style the ripple. Most elements that have a ripple have a `<paper-ripple>` 
in the shadow DOM with an ID of `ink` or `ripple`. For example, to style a 
button:

    paper-button::shadow #ripple {
      color: blue;
    }

To style a checkbox:

    paper-checkbox::shadow #ink {
      color: blue;
    }

### Shadow effect

Material has an apparent elevation (z-height) and casts shadows. In {{site.project_title}},
elements can  have a z-height between 0 and 5. Material can raise or lower in
response to user input.

The `paper-elements` have shadow effects built-in. For example, a 
`<paper-button>` declared  with the `raisedButton` attribute appears raised 
above thesurface it rests on, and raises  up when touched.

<paper-button label="Raised button" raisedButton></paper-button>

When building your own elements or using standard DOM elements, you can use
the `<paper-shadow>`  element to create the appropriate shadow effect.

To apply a shadow to an element, simply add a `<paper-shadow>` element as a
child element. The `<paper-shadow>` element automatically adds the shadow to
its parent  element:


     <div style="width: 100px; height: 100px;">
      <paper-shadow z="3"></paper-shadow>
     </div>

You can change the z-height of the target element by setting `z` on the
`<paper-shadow>`  element. Z values range from 0 (no shadow) to 5.

<div layout horizontal>
  <div class="demo-card">
    <p>z = 1</p>
    <paper-shadow z="1"></paper-shadow>
  </div>
  <div class="demo-card">
      <p>z = 3</p>
      <paper-shadow z="3"></paper-shadow>
  </div>
  <div class="demo-card">
    <p>z = 5</p>
    <paper-shadow z="5"></paper-shadow>
  </div>
</div>


The apparent height of the element (the z-height value) is absolute &mdash;
that is, an  element with a z-height of 3 casts the same size shadow
regardless of the z-heights of  the background elements. In addition, the
z-height does not affect the stacking order of  elements. To change stacking
order of sibling elements, use the `z-index` CSS property as  usual.

You can apply a shadow to a different element (other than the parent element)
by setting  the `<paper-shadow>` element's `target` property. However, the
target must still be an  element that accepts children. (For example, you
can't add a shadow directly to an `<img>`  element.)

**Note:** The `<paper-shadow>` element sets its target to `overflow: visible`
so the  shadows are visible outside of the element's borders. If you need to
clip inner content, use another container inside the shadowed container. 
{: .alert .alert-info }

<a href="/components/paper-elements/demo.html#paper-shadow">
<core-icon icon="arrow-forward" size="16"></core-icon> More examples</a>


## Transitions

Support for transitions is rapidly evolving. The `<core-animated-pages>`
element displays a single child element at a time, and provides support for 
sophisticated transitions between two children, or _pages_.

You can define a set of transitions to be executed when transitioning between
pages. To provide visual continuity across transitions, animated pages support
_hero transitions_, where a selected element on the starting page appears to
morph into a related element on the ending page. Use hero transitions to link
important elements together, while using a simpler transition such as a 
cross-fade for the remaining elements.

For example transitions, see the [`<core-animated-pages>` demos](/components/core-animated-pages/demo.html). 
The <a href="/apps/topeka/" target="_blank">Topeka sample app</a> also 
demonstrates a number of transitions in context.

## Scrolling techniques

The [`<core-scroll-header-panel>`](/docs/elements/core-elements.html#core-scroll-header-panel) 
element supports a number of scrolling effects described in the material 
design spec, including condensing and expanding the toolbar as the user 
scrolls and hiding or showing the toolbar. 

For resizing toolbars, `<core-scroll-header-panel>` lets you define how to 
transition the toolbar's contents between states &mdash; resizing text, 
showing or hiding /components, and cross-fading between backgrounds, for 
example.

See the [`<core-scroll-header-panel>` demos](/components/core-scroll-header-panel/demo.html) 
for some examples of the effects possible.

<script>
  document.getElementById('toast-button')
    .addEventListener('click', function() {
      document.getElementById('toast').show();
  });
  document.getElementById('dialog-button')
    .addEventListener('click', function() {
      console.log('Showing dialog...');
      document.getElementById('dialog').toggle();
  });
</script>
