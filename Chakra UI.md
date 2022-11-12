## What is a Chakra UI?
Chakra UI is a component-based library. It's made up of basic building blocks that can help you build the front-end of your web application.
It is customizable and reusable,and most importantly it supports ReactJs, along with some other libraries too

## Is Chakra UI better than material UI?

### First things first: flexibility =>
The Chakra UI has a much cleaner classNames structure.

For example, look at the HTML source code built into both libraries. You will see that Material UI adds numerous classes to each HTML tag created for material components, whereas Chakra UI adds comparatively fewer classes.

Furthermore, Chakra UI provides easy manual manipulation in CSS classes, whereas Material UI makes it much harder to customize its components. Material UI comes with many more ready-to-use components, but a lot less flexibility in terms of style adjustments.
### ease of use =>
Since Material UI has so many properties and a lot more controls, it requires more time to understand them and decide which component to use in which scenario. Chakra UI is newer, so it is much easier to pick up.

As for documentation, both options are good, but Material UI is an easy choice in this case—although it will, of course, take more time to go through.

In terms of responsiveness, with Material UI there is a need to add separate code to make the controls responsive, whereas Chakra UI provides built-in support and requires very few code changes.

### reliability =>
In terms of reliability and an active community, Material UI is flexing strong muscles here. It has over 900K users (as of publication) on GitHub and a robust community, which makes it the most popular UI framework.

The Chakra UI was created only about two years ago and has more than 90K users as of publication, but this can and will change—during this short period of time, Chakra UI has received a plethora of positive comments from top React developers, as they find it “extensible and customizable.”
### performance => 
Since Chakra UI uses CSS-in-JS (Emotion + Styled System), its welcome flexibility has a small downside when it comes to runtime. This runtime footprint is caused by style computations by Styled System, and className generation by Emotion. If the app you’re developing is performance sensitive and uses high levels of frequently changing data, you might notice this footprint as your app grows.

In general, for small or medium data-driven applications, we think Chakra UI is a terrific option.

## Chakra UI is best known for having:

1- fewer classes for each HTML tag;
2- easy manual manipulation in CSS classes;
3- a robust, layout-focused library;
4-easier-to-pick-up controls (since it's new);
5-composable, flexible, and scalable code;
6-built-in support (fewer code changes);
7-good documentation; and
8-a level of performance that is good for small- to medium-sized, uniquely designed apps. 

## Material UI is best known for having:
1- a large variety of pre-styled UI components;
2-more classes for individual HTML tags;
3- more CSS classes with more components;
4-less facility for the creation of custom components;
5-robust documentation (slightly better than Chakra UI);
6-a more mature and active community; and
7-a level of performance that is great for large, data-driven apps.

If you need something that’s quick on its feet, Chakra UI is the best option, since it is super easy to learn and lightweight.
## How to use Chakra UI?
To use Chakra UI in your project, run one of the following commands in your terminal:

npm i @chakra-ui/react @emotion/react @emotion/styled framer-motion

After installing Chakra UI, you need to set up the ChakraProvider at the root of your application. This can be either in your index.jsx, index.tsx or App.jsx depending on the framework you use.

