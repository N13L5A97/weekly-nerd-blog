# Bramus

## Who is Bramus?

Bramus Van Damme is a web developer from Belgium. He works as a Chrome Developer Relations Engineer at Google, he spreads the word on CSS, UI, and DevTools. Before joining Google, Bramus worked as a freelance developer in various front- and backend roles. For seven years he also was a College Lecturer Web & Mobile, educating undergrad students all about HTML, CSS, and JavaScript.

## View Transitions (Same Document)

View transitions are transitions to another view in the same document. They can be done with the view transition api.

```js
document.addEventListener('click', e=> { if (!document.startViewTransition) { nextSentence(); return;   } document.startViewTransition(() => { nextSentence();   }); })
```

### How it works

The mental model is pretty simple. The browser takes a snapshot of the page before you transition. In the background it changes the page and then takes a snapshot of the new page and switches seamless between the to snapshots. With animations you can tweak this transition to your liking.

There are just 3 steps that need to be done:

1. Apply names on all the elements that are transitioning
2. Trigger the view transition
3. customize the css animation

view-transition.png

## Cross-Document View Transitions

Cross document view transitions mean that this seamless transition can also be done through multiple pages. This has 2 conditions. They need to have the same origin otherwise it won't work and cross-Document view transitions are opt-in. For the rest of it, it is basically the same thing and "You no longer need to rearchitect your website to an SPA to use View Transitions".

## Reflection

The start of the talk was really nice. I could follow a lot of what he was saying and I thought it was really cool you could do stuff like this. In the end he really lost me. The talk was really long and I couldn't follow anymore. I did understand the way view transitions work by the browser taking snapshots of the versions and then switch them. So I think I understood most of his presentation. At first I thought view transitions were just cool animations that overlay the page to make it look cooler when you switch pages, but I never thought you could actually move elements in your view when going to another page. This is amazing!
