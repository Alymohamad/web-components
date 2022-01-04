# web-components
Web components Blog - Web Engineering Wahlpflichtmodul

##### Table of Contents  
* [What are Web Components?](#whatare)  
* [Why and when to use Web Components?](#whyuse)  
* [How do they work?](#howwork)  
* [Libraries and templates](#libraries)

<a name="whatare"/>. 
## What are Web Components?

JavaScript frameworks like React and Angular have long allowed developers to define reusable web elements. However, each framework uses a different standard, which prevents the practical code snippets from being used across projects in many cases. This is achieved by the so-called Web Components, which are reusable HTML components that can be used independently of the framework. The web element type, which was standardized in 2012, is now supported by every common browser.

So we can conclude that Web Components are reusable client-side components based on official web standards and supported by all major browsers. They are an excellent way of encapsulating functionality from the rest of our code. Not only that, but we can reuse them in every web application and web page in multiple projects. Web Components also enable us to develop entirely independently of frontend frameworks. 

The Web Components model, published as a standard in 2012, primarily provides for the following four specifications for creating useful HTML components:

* Custom Elements: set of JavaScript APIs for defining custom elements.
* Shadow DOM: set of JavaScript APIs for adding DOM elements
* ES Modules: modules for embedding and reusing JavaScript documents
* HTML Templates: mark-up templates that are not mapped to the rendered page and can be used as the basis for custom elements

The latest version of the standard ist the following from 2014 https://www.w3.org/TR/components-intro/

<a name="whyuse"/>. 
## Why and when to use Web Components?
Libraries and frameworks such as Angular react or jQuery have been among the most important tools of every web programmer for years. But as practical and versatile as these code frameworks are, which save a lot of work in the development of projects, they often prove to be inflexible when it comes to cross-project use. Ehich becomes mostly visible when migrating an already existing project or when setting up a new project. In the case of the latter since we cant reuse the already existing components in another framework we will loose time developing the same components for the new framework again. This is why the reusablity of the components bacame important in the latest years. For this reason, the World Wide Web Consortium (W3C) introduced Web Components, and with it a universal framework for easy, cross-application reuse of HTML, CSS, and JavaScript code. The use of standards makes systems more tolerant to change. Even React itself is suggesting the use of Web Components in their official documentation https://reactjs.org.



<a name="howwork"/>. 
## How do they work?

The Web Components concept is fundamentally based on four specifications, which we will be discussed in the following section in more detail:

### Custom Elements

Here's an example of how define and integrate the web componet into a HTML page:
Custom elements are HTML tags that encapsulate the content of HTML, including CSS instructions and scripts. To create a custom element, you need JavaScript and the define method. The following Web Components sample shows an example of a custom element

```
class MyWebComponent extends HTMLElement {...}
window.customElements.define('my-web-component', MyWebComponent);

<my-web-component></my-web-component>
```


### Shadow DOM

The most important feature of Web Components is their ability to encapsulate HTML elements. The Shadow DOM API helps you do this by allowing you to attach hidden DOM trees to a document tree. In this case, only the HTML tag of the shadow DOM is visible. This allows you to add HTML elements to the hidden DOM without having to modify the main DOM each time as well. More information can befound under the following link https://www.ionos.at/digitalguide/websites/web-entwicklung/was-ist-der-shadow-dom/


### ES Modules

ES Modules are modules that export objects, functions, or variables from a JavaScript file. This property allows variables within a file to be divided into groups in a meaningful way and referenced.

To export a function from a JavaScript library, you use the export method. In the example, you export a function that returns an input string twice.

```
// ? lib.bib1
export const wiederhole = (string) => `${string} ${string}`;
}

```

Via import you can now call the exported function as often as you like.
```
 main.mjs
import {wiederhole} from './lib.mein';
wiederhole ('Hello');
// → 'Hello Hello'
```


### HTML-Templates
An HTML template is a template for HTML files. The contained elements remain inactive and unrendered until they are explicitly called. Due to this property, they have no negative effect on the loading time of a web page. They are therefore a useful alternative to the conventional JavaScript methods. As follows:

```
<template id="mein-element">
<p>Mein Element</p>
</template>
```

And then you can use the template in a web page as follows:
```
let template = document.getElementById('mein-element');
let templateContent = template.content;
document.body.appendChild(templateContent);
```


<a name="libraries"/>. 
## Libraries and templates
Especially as a beginner, programming Web Components can be complicated. However, on the Internet you will find numerous libraries with templates and standard functions, as well as practical examples of Web Components, which will make your work easier.

* Lit Element: simple base class for creating Web Components.
* Polymer Project: google provides a starter kit for programming apps with Web Components, an HTML template library for JavaScript, and a wide variety of ready-to-use elements.
* Hybrids: provides simple UI library for creating Web Components.
* Slim.js: library with advanced features for Web Components that uses class-based inheritance from JavaScript ES6.

