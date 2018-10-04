 Vue.js synopsis

The good
Components
I really like the component specific styling. Css scoped/module styles. Allows for scss. Uses css modules for reusable css, with theming. (https://github.com/css-modules/css-modules/blob/master/docs/theming.md, https://www.netguru.co/codestories/vue.js-scoped-styles-vs-css-modules): COUNTER ARG: CSS-in-JS and why not just use javascript as the preprocessor?
I like how you can define the templates, styles and javascript in any order in the file. This causes another thing to need to come to an agreement in the team about but allows for better visibility into what the component is first (html, what the javascript related to it is, and THEN usually the least important peice is knowing what the styles associated to it are so those can come last).
Console logging imported components is GOLD. In react you get a class or function as a string. In View, you get the exported object which really helps for debuggability and insight from the console.
I like how you can emit things from children components as opposed to having to pass down functions as props to use as handlers.
I like how prop types are using the native javascript object declarations to determine the type of the variable. This limits your ability to refine what you want, but it is built in and just works as expected for simple cases. COUNTER ARG: This isn't needed with a statically typed implementation.
Class manipulation is built in and slick. e.g.: `<div class="grid " :class="{ column: isColumn }">`


The bad
You cannot export more than one component from a file from what I can tell. This is very easy in React. This makes it harder to reuse templates in the same file even, since there is a one template per file rule. (https://hackernoon.com/writing-multiple-vue-components-in-a-single-file-199871f6182e)
I need to not only import each component that I am going to use, but specify them in a "components property for the export in the script tag. This is duplicated work, extra verbose and seemingly unnecessary.
I need to specify props that are strings like :propName="'string passed down'" instead of just passing an idomatic javascript string like propName="string passed down".
You need to use "slots" to pass children down. This seems extra tedious than just specifying children. Maybe a nit pick, but it seems more simply implemented in React.
No such thing as fragments, so everything must be wrapped in a top level element within the template tag.
The are render functions  that emmulate what react does, but this isn't ideomatic Vue. One out of every 10-15 components may use this, but then you have to go into a syntax that is now not familiar. With React, you always go striaght to the render method and there are no suprises when there is not one (which you may have in vue when there is no template html block)
Having named slots is confusing when labeling the slot as a prop on another component. As a developer new to Vue, I see a prop passed into a component and then go to that component but there is no reference of it there.
State is mutable at the core, this might be slightly faster but not the preferred way to manage state and can lead to all kinds of issues.


Questions
I cannot find a way to use scss with css modules and reference nested css module classes. This limits your ability to compose and write less redundant code by nesting.