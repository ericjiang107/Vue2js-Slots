<template>
  <div>
    <form-helper>
      <!-- using slots to pass -->
      <!-- we can give the slots different names in order to move them around individually -->
      <!-- <h2 slot='name1'>
        Slot title using {{ title }}
      </h2>
      <p slot='name2'>
        Paragraph text
      </p> -->

      <!-- for the form header -->
      <div slot='header'>
        <h3> {{ title }} </h3>
        <p>Information about form here</p>
      </div>

      <!-- for the form fields -->
      <div slot='fields'>
        <input type="text" placeholder='name' required> 
        <input type="password" placeholder='password' required> 
      </div>

      <!-- for the form controls -->
      <div slot='controls'>
        <button v-on:click='handleSubmit'>
          Submit
        </button>
      </div>

    </form-helper>

    <hr>

    <form-one></form-one>
    <form-two></form-two>

    <!-- in order to retain the input data/data while still rendering back and forth, we can use the keep-alive tag -->
    <keep-alive>
    <!-- instead of using form-one and form-two, we can use the component tag -->
    <!-- component is data binded to form-one as shown in data -->
    <component v-bind:is="component"></component>
    </keep-alive>

    <!-- creating a button to switch between form-one and form-two -->
    <button v-on:click="component = 'form-one'">
      Show Form One
    </button>
        <button v-on:click="component = 'form-two'">
      Show Form Two
    </button>
  </div>
</template>

<script>
import formHelper from './components/formHelper.vue';
import formOne from './components/formOne.vue';
import formTwo from './components/formTwo.vue';

export default {
  components: {
    'form-helper': formHelper,
    'form-one': formOne,
    'form-two': formTwo,
  },
  data () {
    return {
      title: 'title written in App.vue data object',
      component: 'form-one'
    }
  },
  methods: {
    
  },
}
</script>

<style>

</style>
