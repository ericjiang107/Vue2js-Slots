<template>
  <div>
      <slot name='name1'></slot>
      <h1>Form Helper</h1>
      <!-- adding the slot tag from App.vue to output whatever we put there here -->
      <slot name='name2'></slot>

      <hr>

      <!-- having a form -->
      <h1>Please fill out form...</h1>
      <form action="">
          <div id="form-header">
              <!-- custom header -->
              <slot name='header'></slot>
          </div>
          <div id="form-fields">
              <!-- custom fields -->
                <slot name='fields'></slot>
          </div>
          <div id="form-controls">
              <!-- custom controls -->
                <slot name='controls'></slot>
          </div>
          <div id="useful-links">
              <!-- list of links -->
              <ul>
                  <li>
                      <a href="#">Link 1</a>
                  </li>
                  <li>
                      <a href="#">Link 2</a>
                  </li>
                  <li>
                      <a href="#">Link 3</a>
                  </li>
              </ul>
          </div>
      </form>
  </div>
</template>

<script>

export default {
  components: {

  },
  data () {
    return {
      
    }
  },
  methods: {
    
  },
}
</script>

<style scoped>
    h1 {
        color: red;
        text-align: center;
    }

    #form-header {
        background: #ddd;
        border: 1px solid black;
    }

    form > div {
        padding: 20px;
        background: #eee;
        margin: 20px 0px;
    }

    #useful-links li {
        display: inline-block;
        margin-right: 10px;
    }
    
    #useful-links ul {
        padding: 0px;
    }

    form {
        width: 100%;
        max-width: 960px;
        margin: 0px auto;
    }

</style>