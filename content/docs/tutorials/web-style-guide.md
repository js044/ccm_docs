# Web Style Guide [WIP]
Our website has gone through several, several iterations, and the goal is to ultimately rework it again with Tailwind CSS instead of Bootstrap. This style guide is meant to be a dynamic document that can help provide structure to our design vision even as we grow and change. 

## Colors
One of the most formative elements of our visual branding is our color schemes/themes.

> (placeholder until there are more formal graphics)

```
:root,
  :root.white {
    --bg-color: #FFF;
    --text-color: #4f4f4f;
  }
  :root.yellow {
    --bg-color: #FFF380;
    --text-color: #fc723f;
  }
  :root.red {
    --bg-color: #fc723f;
    --text-color: #FFF380;
  }
  :root.green {
    --bg-color: #94EFA2;
    --text-color: #5b72f5;
  }
  :root.blue {
    --bg-color: #5b72f5;
    --text-color: #94EFA2;
  }
  :root.pink {
    --bg-color: #f3a49e;
    --text-color: #FFF380;
  }
```

## Typography
We use Inconsolota, Nimbus sans, and Raleway.

## Web components
One of our major efforts has been to design a cohesive CSS design library that prioritizes reusable CSS. There are [many](https://nicolasgallagher.com/about-html-semantics-front-end-architecture/) [reasons](https://adamwathan.me/css-utility-classes-and-separation-of-concerns/) for this. As such, we have developed a few content-agnostic components:
