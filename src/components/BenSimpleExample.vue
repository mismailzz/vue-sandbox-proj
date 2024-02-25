<script>
export default {
  data: () => ({
    textColor: "black",
    message: '', // This will hold the text input value
    checked: false,
  }),
  methods: {
    changeColor(color) {
      this.textColor = color; // Update the text color based on the button clicked
    },
  },
};
</script>

<template>
  <div>

    <!-- v-bind for dynamically update the attributes like we are changing the color on click
    or similarly we can do for the links-->
    <h2>v-bind Example</h2>
    <h4 :style="{ color: textColor }">Dynamic Text Color</h4>
    <button @click="changeColor('red')">Red</button>

    <h2>v-model Example</h2>
    <!--
      v-model is a Vue.js directive that creates a two-way binding on an input, textarea, or select
      element. It automatically picks the correct way to update the element based on the input type.
      This makes it very useful for creating forms or input fields that update the Vue instance's 
      data in real-time, as the user types or changes values.
    -->
    <input v-model="message" placeholder="Type something here...">
    <p>The message is: {{ message }}</p>

    <!-- Ex.2 Checkbox Binding-->
    <input type="checkbox" v-model="checked">
    <label>Check me</label>
    <p>Checked: {{ checked }} </p>



 </div>
</template>