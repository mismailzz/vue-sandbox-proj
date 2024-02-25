<script>
    export default {

    data: () => ({
        increment_counter: 0,
        tens_counter: 0,
    }),
    computed: {

        event_status(){

        let temp_status = "NOT FOUND"
        if (this.increment_counter % 10 === 0 && this.increment_counter !== 0){
            temp_status = "FOUND"
        }else {
            temp_status = "NOT FOUND"
        }
        return temp_status
        }

    },
    watch: {
        // Watch the increment_counter for changes
        increment_counter() {
        // Every time increment_counter changes, check if it's a multiple of 10
        if (this.increment_counter % 10 === 0 && this.increment_counter !== 0) {
            this.tens_counter += 1;
            /*
            Last code use with computed:
            The code snippet you've provided has a logical issue within the computed property 
            tens_counter. In Vue, computed properties should be used to calculate a value based 
            on reactive data properties and should not be used to modify or depend on themselves 
            for updates because they are meant to be pure functions. That means the value of a 
            computed property should only depend on other reactive properties and should not 
            cause side effects like changing data properties or other state within the component.
            */
        }
        }
    },
    methods: {
        incrementMe(){
        this.increment_counter += 1;
        }
    },
}
</script>

<template>
<div> <!--Need to create a separate div because to make it root otherwise below element 
get confused who is root-->
    <!-- Simple Counter -->
    <p>Increment: {{ increment_counter }}</p>
    <button @click="incrementMe"> Increment </button>

    <!-- Monitor 10's increment -->
    <p>10's Increment: {{ tens_counter }}</p>

    <!-- Found Event or Not -->
    <p>10's Event: {{ event_status }}</p>
</div>

</template>