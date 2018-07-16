<template lang="html">

  <div class="modal" :class="openModal">
    <div class="modal-background"></div>
    <div class="modal-content">
      <div class="box">

      <form>
        <div class="field is-grouped">
          <input class="input" type="text" name="first" required placeholder="FIRST NAME" style="max-width:49%; margin:auto; text-align:center; font-style:uppercase;">
          <input class="input" type="text" name="last" required placeholder="LAST NAME" style="max-width:49%; margin:auto; text-align:center; font-style:uppercase;">  </div>

        <div class="field">
          <input class="input" type="email" name="email" required placeholder="EMAIL" style="max-width:100%; float:left; margin: auto; text-align:center; font-style:uppercase;">
        </div>

        <br><br>

      <div style="min-height:50px; margin:0px 15px 0px 15px;">

            <div class="form-check" style="float:left; margin:10px 15px 15px 15px; text-align:left; min-width:30px;">
              <input type="checkbox" required class="form-check-input" id="exampleCheck1">
              <label class="form-check-label" for="exampleCheck1">I agree to receive updates, alerts and promotions from CBS and that CBS may share information about me with their marketing partners so that they may contact me by email or otherwise about their products or services.</label>

            </div>

              <br>
              <br>

            <div class="form-check" style="float:left; margin:10px 15px 15px 15px; text-align:left; min-width:30px;">
              <input type="checkbox" required class="form-check-input" id="exampleCheck2">
              <label class="form-check-label" for="exampleCheck2">I agree to the terms and conditions of the CBS <a href="https://www.cbsinteractive.com/legal/cbsi/privacy-policy">Privacy Policy</a> and <a href="https://www.cbsinteractive.com/legal/cbsi/terms-of-use"> Terms of Use</a>.</label>
            </div>

            <br>
            <br>

            <div class="form-check" style="float:left; margin:10px 15px 15px 15px; text-align:left; min-width:30px;">
              <input type="checkbox" required class="form-check-input" id="exampleCheck3">
              <label class="form-check-label" for="exampleCheck3">I hereby certify that I am 18 years of age and consent to having my photo posted on CBS social media accounts.</label>
            </div>

            <br>
            <br>


      </div>

        <br>
        <br>

          <button type="submit" class="button is-medium" style="min-width:100%;">Submit</button>
      </form>

      </div>
    </div>
    <button class="modal-close is-large" @click='close' aria-label="close"></button>
  </div>

</template>

<script>

import db from './firebaseInit'

export default {

  props:['openModal'],

  name: 'Modal',

  methods:{
    close(){
      this.$emit('closeRequest')
    }
  }

}
</script>

<style lang="css">
</style>
