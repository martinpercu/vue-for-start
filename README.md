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
