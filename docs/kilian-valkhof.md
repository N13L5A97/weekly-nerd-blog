# Week 1

Killian Valkhof (he/him)
Founder Polypane

## Who is Killian?

Killian is a front-end developer, user-experience designer and generalist.  He is a part of Electron Governance and is the founder of Polypane. He also has been building websites for 20 years.

## The rule of the least power

Killian believes in the principal of the rule of least power. This means you should choose the least powerful language for the give purpose. Meaning you should build as much as you can with HTML if that can be done and if not switch to CSS and if you can’t do it with css build it with Javascript. In this article you can read about some techniques Killian uses.

## Custom Toggles

Some input elements, like checkboxes, are hard to style because every browser has their own styling for this. To keep the functionality but make it look better you can set the display to none and use the pseudo class :before to give it a nice styling.

You can use this technique to make a switch instead of a checkbox. Safari has a build in attribute so the browser knows if its a switch

```html
<input
    type="checkbox" switch
/>
```

## Datalist

The datalist element gives you the opportunity to autocomplete the users input.

```html
    <input/>
    <datalist>
        <option>1</option>
        <option>2</option>
        <option>3</option>
        <option>4</option>
    </datalist>
```

[image of datalist]

## Colorpickers

A lot of people still use Javascript to make color pickers. This can also be done in HTML:

```html
<input type="color">
```

## In-page transitions

With HTML you are perfectly able to make smooth transitions to other sections of your page. You can just use the id of an element as anchor and set its parent to scroll-behavior.

```css
    html{
        scroll-behavior: smooth;
    }
```

To keep this accessible you can add this motion to a media query for reduced motion:

```css
    @media( prefers-reduced-motion: no- preference ){
     html{
         scroll-behavior: smooth;
   }
    }
```

To make sure you give the section a little more space you can add a scroll margin:

```css
my-target{
    scroll-margin-top: 100px;
}
```

## Fixed/Sticky Styling

If you want a fixed element on your page for a certain area you can use the position sticky property.  Now it will stick inside the parent element and it wont disappear from the structure.

```css
    div{
        position: relative;
    }

    div > .sticky{
        position: sticky;
        top: 0;
    }
```

## Carousels / Sliders

You can make amazing sliders with no use of any Javascript. Just set scroll-snap type on the parent element.

X or y will tell the direction.
Mandatory lets the items always snap to its next position.
Proximity lets the items only snap when at the edge.

```html
  <div class="container">
        <div> 1 </div>
        <div> 2 </div>
        <div> 3 </div>
    <div>
```

```css
.container{
    scroll-snap-type: y mandatory;
}

div{
    snap-align: center;
}
```

You can also use snap align on the children. You can use start, end or center to tell the child where to snap to.

## Accordions

Accordions are really easy to make with the html element details. The summary will always be visible and everything else in the element will only be visible when opening. The default state of a details element is closed but you can override this with the open attribute.

```html
  <details open>
         <summary>titel</summary>
         <p>dit is automatisch verborgen</p>
     </details>
```

## Models

A dialog is a html element just a modal. This is often done with an alert but an alert stops all javascript until the user has done something, and you do not want that to happen. On default you do not see this dialog so you do need javascript to open it. If there is a form element in the dialog, it will the the submit entry as a fulfilled dialog.

```html
    <dialog>
        <form>
            <h1>TItel<h1>
            <button >SEND</button>
        </form>
    </dialog>

  <button onClick="$$('dialog').showModal()"> </button>
```

You can style the back of the dialog with the backdrop pseudo selector.

```css
 dialog::backdrop{
      background: #ffffff;
      backdrop-filter: blur(4px)
     }
```

## Reflection

I learned a lot of cool new techniques to avoid overusing javascript. This is not only easier for me but also give the user a better experience. By using the least powerful tools makes the foundation stronger in the end. I know the more Javascript you write the heavier the website gets so for me this has been really helpful understanding new ways to improve my developer skills. I think one of the coolest features that was  mentioned is the data list element. I wouldn’t even know how to build this myself and I think it’s a great tool to improve the user experience.
