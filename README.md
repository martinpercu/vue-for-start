# Start Vue from Zero

## Start 
- In the index.html in the body <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>. This will bring the VUE!!!
- The "Vue.createApp" mount(#app) will create the app used in a div with id="app"

## Data Interpolation 
- In the "Vue.createApp" using templates.
- v-text="text" ===> will take the var text
- v-once ===> will show the var text just one time and will not be possible to change the render of this.
- v-html ===> if var is somethig like "<h2>BLALBLA</h2>" will interpreter well. (of course not allow to user ... is probably someone inject some malicious scripts!!).

## Reactive Atribute 
- Clean all the index.html. I will left an index-old-01.
- the template for an img ===> IMPORTANT we can bind also the attribute as the "src".

## User Events 
- Clean all the index.html. I will left an index-old-02.
- Just to see how works ===> v-on:click + v-on:keyup + v-on:submit + v-on:submit.prevent