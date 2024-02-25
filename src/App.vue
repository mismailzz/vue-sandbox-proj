<script>
import IncCounter from './components/IncCounter.vue'
import BenSimpleExample from './components/BenSimpleExample.vue'
import propsExample from './components/propsExample.vue'

export default {
  components: {
    IncCounter,
    BenSimpleExample,
    propsExample,
  },
  /*Adding @bencodezen code*/
  data() {
    return {
      characterList: [
        {"Goku": "Ultra-Instict"},
        {"Vagita": "Goat of Destruction"}
      ],
    }
  },
}

</script>

<template>
  <div id="app">
    <IncCounter />
    <BenSimpleExample />
    <propsExample :character="characterList"/> <!--we can also pass func. from parents but not 
    recommended approach because parent need to do lot of stuff. Will study a bit later that why
    we dont use props for passing func. Now we are binding dynamic variable and passing to 
    component. Its kind of passing the properties to the components, on which child will work like
    kind of a func-->

    
  </div>
</template>
