# Nils Binder

## Who is Nils?

Is from Germany and is Front-end designer at 9 Elements.
Is very passionate about origami.

### 9 Elements

At 9 Elements has a structure with 3 units:

- Communication design (non-coding designers)
- Product Development
- Web Development (produce small/medium websites)

These units work closely together.

## The Wrapper Element

The wrapper element is a container for all the content.
This has a max-with a padding and a margin. This can be done in multiple ways.

<!-- before -->
.wrapper{
    max-width: 75rem;
    margin: 0 auto;
    padding: 0 1 1.5rem;
}

<!-- shorter -->
.wrapper{
    width: min(100% - 3rem , 75rem);
    margin-inline: auto;
}

<!-- even shorter ?????-->

.wrapper{
    margin-inline: max(1.5rem, ((100%-75rem) /2 ));
}

You can use custom properties for the values.

## Figma

Figma is a great tool for designers to design for web. A lot of controls are similair to the ones in CSS. Which make it much easier for developers to recreate a design.

BUT

When designing we mostly design for a fixed canvas.

### Units

Most units in Figma are pixels or %. In dev mode you can convert this to rem.

In CSS you have px % rem ch ex em. AND you have a lot of viewport units.

## Optional Column Technique

It's a column based on 4 column.

.fancy-text{
    display: grid;
    grid-template-colums: 2fr 3fr auto 1fr;
}

With this technique the communication between design and development goes more smoothly.

Think about what happens on big screens. When do you center the wrapper and give a lot of whitespace and when do you make use of it.