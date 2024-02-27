# Start Vue from Zero

## Start 
- In the index.html in the body <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>. This will bring the VUE!!!
- The "Vue.createApp" mount(#app) will create the app used in a div with id="app"

# Declarative Render
## Data Interpolation 
- In the "Vue.createApp" using templates.
- v-text="text" ===> will take the var text
- v-once ===> will show the var text just one time and will not be possible to change the render of this.
- v-html ===> if var is somethig like "<h2>BLALBLA</h2>" will interpreter well. (of course not allow to user ... is probably someone inject some malicious scripts!!).

## Reactive Atribute 
- Clean all the index.html. I will left an index-old-01.
- the template for an img ===> IMPORTANT we can bind also the attribute as the "src".

# User Inputs
## User Events 
- Clean all the index.html. I will left an index-old-02.
- Add before the "template" the "methods{}" we will use.
- Just to see how works ===> v-on:click + v-on:keyup + v-on:submit + v-on:submit.prevent

## Reactive Inputs 
- Clean all the index.html. I will left an index-old-03.
- Use all kind of input + value and dif reactives ways.
- Important "v-on:" == "@"  and  the "v-bind:" == ":"
- Clean all the index.html. I will left an index-old-04.
- The last one to connetc everything without using methods is ===> "v-model" 

# Reactivity
## Computed Properties
- Clean all the index.html. I will left an index-old-05.
- We use the "computed:" here we declare funtions with the same name as the variable will represent. In this case is fullName() that is invoce que html with {{ fullName }}.  SAME NAME  """Function <==> Variable"""
- Another example with "today".

## Watchers
- Clean all the index.html. I will left an index-old-06.
- We use the "watch:" here que declare function "with the same name as variables" to watch if they change it. 
- Important... the whatchers should make just 1 thing.

## Reactive Styles
- I will left an index-old-07.
- In the index 3 ways to inser the styles in the container. 
- 1 Using v-bind:style="superstyles"
- 2 Using v-bind:class="{ 'opened': open, 'closed': !open }
- 3 Using v-bind:class="ourStyles" ==> ourStyles is a method comming from "computed:"

# List and Conditionals
## Conditionals
- I will left an index-old-08.
- Now we delete (I left commented) the computed method buttonLabel().
- And replace the  {{ buttonLabel }} in button with 2 divs!!!
- Now we add an input to pass an username to access.
- This variable is declared in data as an empty string. 

## Lists
- I will left an index-old-09.
- In data create a list of posts.
- Then for render this list use the v-for.
- IMPORTANT to control each element and be able to destroy an item or add other use the attribute ":key"
- :key if mandatory to add something to identify it. In this case in the same v-for the for cycle is bring the "item" and "i". This "i" is in attribute key.  ==> "i" is index!!! With that in the DOM each item has an unique identifier.

# Components personalized
## Components
- I will left an index-old-10.
- First steps to isolate element to convert them in a "component"
- Separete the "Vue.createApp" from the ".mount"
- A grosso modo ==> const vm = Vue.createApp change to const app = Vue.createApp
- A grosso modo ==> .mount("#app"); change to const vm = app.mount("#app");
- NOW ==> app.component("item", { json with all we want to use })
- In the JSON we add: a "template:" here we put the component.
- In the JSON we add: a "props:" here ad an indentifier to connect to it.

## Slots
- I will left an index-old-11.
- In the app.component(v-layout, {template}).... v-layout is the name will be invoked fromo the app.
- The <slot> is where we add the name will be invoke in the <template> inside the v-layout
- As example "<slot name="header-top"></slot>" is inside a <header> And this will works fine also. "The slots can use any name"

# Communicatino between components
## From father to child
- I will left an index-old-12.
- This is just the example to connect the father to one child.
- Just use the "v-bind:" In this case I usea "itemo" just to show has no relation with the "v-item" (component name).

## From child to father 
- I will left an index-old-13.
- This is just the example to connect the child to the father.
- The way Vue allow us to connect from the child is using "events" so we must prepare the father to listen the event and the child to generate.
- So in father => "v-on:event_example="remove(i)". Where remove(i) is the method to remove this item.
- In the child => "v-on:click="eventToFatherGenerator" Where eventToFatherGenerator is the method to generate the event "this.$emit("event_example")".

## Custom V-MODEL 
- I will left an index-old-14.
- This is an example to use like a doble connection.
- The father component with this <v-inputa v-model:someValue="textInput" /> send and receive. In this case is sending the "textInput"
- In child component use "v-bind:value="someValue"" to get the "textInput" from the father but also with "v-on:input="inputa"" will send with the method "inputa" the "emit" to UPDATE the "someValue".

## Deep component communication 
- I will left an index-old-15.
- With "provide" we declare something to use everuwhere.
- With "inject" we get what there is in "provide".
- The simple "provide" is like lines 18,19,20 (Already commented). If we want to use in this provide other vars from the same component the "provide" must be "provide()" returning something. This convert the provide in a reactive elememnt.

## Component instance 
- I will left an index-old-16.
- This is just example to see how Vue could be use just in part over a vanilla js. 
- With the examples console.log with "$" we get the value of the parts in Vue.  

## One .vue file
- Just this a .vue file