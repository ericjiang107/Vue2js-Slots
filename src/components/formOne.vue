<template>
    <div>
        <form-helper>
            <div slot='header'>
                <h3>Form One - Contact Us</h3>
                <p>Fill in this form to contact us</p>
            </div>

            <div slot='fields'>
                <input type="text" placeholder='name' required>
                <label>Your Message: </label>
                <textarea></textarea>
            </div>

            <div slot='controls'>
                <button v-on:click='handleSubmit'>Send</button>
            </div>
        </form-helper>
    </div>
</template>

<script>
import formHelper from './formHelper.vue';

export default {
    data(){
        return {

        }
    },
    methods: {
    }
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