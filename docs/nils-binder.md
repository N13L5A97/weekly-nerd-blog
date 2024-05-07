# Nils Binder

## Who is Nils?

Nils is from Germany and is Front-end designer at 9 Elements. He is also very passionate about origami and spends hours folding paper. Nils moves between two worlds — continuously striving to improve the communication between designers and developers.

## 9 Elements

9 Elements is an agency based in Germany that helps clients building digital products and services, and bringing them to market. At 9 Elements they have a structure with 3 units:

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

Figma is a great tool for designers to design for web. A lot of controls are similar to the ones in CSS. Which make it much easier for developers to recreate a design. BUT... When designing we mostly design for a fixed canvas.

### Units

Most units in Figma are pixels or %. In dev mode you can convert this to rem. Rem is a unit that stands for root em, meaning that the size is relative to the size of the root element.

In CSS you have px % rem ch ex em. AND you have a lot of viewport units which can be used to make your website more responsive.

## Optional Column Technique

Nils had an optional column technique. For this he uses a column based on 4 columns.

.fancy-text{
    display: grid;
    grid-template-columns: 2fr 3fr auto 1fr;
}

This column can be used by the designer and developer. With this technique the communication between design and development goes more smoothly.

## Extra tips

- Think about what happens on big screens.
- When do you center the wrapper and give a lot of whitespace and when do you make use of it.

## Reflection

To be honest I forgot to write the reflection after Nils talk so I don't remember that smoothly what the moral of his story was. The thing I remember was that he wanted to give us some tips on how to improve communication between designer and developer. It is really important that they are on the same page but also give each other the space to work together. It is common the designer creates amazing but almost impossible designs to create with code but also doesn't know what the developer is capable of. The thing I learned most from this talk is to keep in touch with the designer en help each other out. Know each others strengths and weaknesses.

socials:
https://www.linkedin.com/in/nils-binder-91b06414b/

https://ichimnetz.com/

codepen: https://codepen.io/enbee81