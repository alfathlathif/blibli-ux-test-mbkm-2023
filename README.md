<h1>Written Test</h1>

### 1. What is a JavaScript Framework and explain about Vue.js as one of the JavaScript Framework!

Developers employ pre-written, standardized libraries, best practices, and tools called JavaScript frameworks to create web applications. These frameworks give programmers an organized basis for writing, organizing, and maintaining code, which facilitates the creation of scalable, efficient, and maintainable applications. Features like data binding, templating, routing, and state management are commonly found in JavaScript frameworks.

One of the well-liked JavaScript frameworks for creating user interfaces is called vue.js. The term "progressive framework" is frequently used to describe it since it may be gradually implemented into ongoing projects. Vue.js has the following important features:

- Declarative Rendering: The template syntax in Vue.js is written declaratively. To connect the DOM to the data of the underlying Vue instance, you can define templates using a syntax similar to that of HTML.
- Component-Based Architecture: Vue.js encourages the usage of components, which are independent, reusable code segments. Code management and upkeep are facilitated by components, which contain HTML, CSS, and JavaScript logic.
- Reactive Data Binding: The reactivity approach offered by Vue.js enables data changes to instantly update the corresponding DOM elements. Maintaining synchronization between the UI and the application state becomes easier as a result.
- Vue.js offers directives such as v-if, v-for, and v-bind, which facilitate the addition of dynamic behavior to the DOM. This allows for two-way binding. Using the v-model, two-way data binding is accomplished.
- Routing and State Management: Although Vue.js is essentially a view layer framework, it can be combined with other libraries to create complicated single-page applications (SPAs), such as Vue Router and Vuex, with ease.

Vue.js is renowned for being straightforward, adaptable, and simple to include into already-existing projects. Because of its low learning curve, both novice and seasoned developers can use it.

### 2. What is the use of ellipsis?

Typically, "ellipsis" refers to the text-overflow: ellipsis; CSS attribute. Although it has nothing to do with Vue.js, it is frequently used to manage text overflow in HTML elements when combined with Vue.js templates.

When text inside an element exceeds the content box, it should be truncated with an ellipsis (...). This is indicated by the text-overflow: ellipsis; attribute. This is frequently utilized in scenarios where there isn't much room to display text, as in a table cell or a fixed-size container.


### 3. Explain animation properties below:

- @keyframe: The CSS at-rule @keyframes is used to specify a series of style changes in an animation. You can use it to make animations by progressively switching between different CSS style sets. It is defined by referencing the animation-name property after using the @keyframes keyword and a name.
- animation-name: The name of the @keyframes rule that has to be applied to the chosen element is specified by the CSS property animation-name. It alludes to the keyframe rule identifier, which defines the behavior of the animation.
- animation-duration: The CSS property animation-duration determines how long the animation will last. It indicates how long a single cycle of the animation should take. Typically, the value is given in milliseconds (ms) or seconds (s).
- animation-iteration: It appears that your query may contain a typo. The CSS property animation-iteration-count, which specifies how many times an animation cycle should be played before ending, is the one that should be used. For example, an integer can be used to indicate two iterations, or the keyword infinite can be used to indicate an infinite number of iterations.
- animation-direction: The CSS property animation-direction specifies if the animation should play backwards on alternate cycles. It accepts the following values: reverse, alternate, alternate-reverse, and normal (default). Alternate, for instance, would cause the animation to play backward on even iterations and forward on odd iterations.

  
### 4. Please explain how lazy load works in JavaScript!

In JavaScript, lazy loading is a strategy that waits until specific resources—like scripts, pictures, or stylesheets—are actually needed before loading them. This can speed up the loading of pages, particularly for those with a lot of resources or content. The concept is to load the website with only the most important content at first, and load more content as the user interacts with the page.

Here's a simple rundown of how JavaScript handles lazy loading:

- Determine the resource's needed time: The resources (such as pictures and scripts) that can be loaded in a lazy manner based on predetermined criteria—like when they enter the viewport or when a particular event takes place—are identified by developers.
- Determine the resource's needed time: The resources (such as pictures and scripts) that can be loaded in a lazy manner based on predetermined criteria—like when they enter the viewport or when a particular event takes place—are identified by developers.
- Use Intersection Observer or attach an event listener: JavaScript event listeners, such as the scroll event, allow developers to verify whether a resource is in the viewport or whether a particular condition is satisfied. As an alternative, more effective and performant slow loading can be achieved with the Intersection Observer API.
- When necessary, load the resource: The real resource is loaded dynamically when the condition is satisfied, such as when the resource enters the viewport.

### 5. Mention at least 5 git commands and describe each function of them!

- git clone: You can obtain a local copy of the complete project, including its history, by using this command to clone an existing repository.
- git add: To prepare modifications for the upcoming commit, use this command. Git add. allows you to target specific files or stage all changes.
- git commit: The staged modifications are saved to the local repository by using this command, and a brief explanation of the changes is supposed to be included in the commit message.
- git push: This command applies the commits from a designated local branch to a remote repository. It is usually used when you wish to update the remote repository or share local commits with others after making them.
- git pull: You can use this command to pull changes from the remote repository into your local repository. It automatically carries out a git fetch and git merge.
