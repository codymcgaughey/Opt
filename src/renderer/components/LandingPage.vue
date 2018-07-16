<template>
  <main>
    <div id="image">

      <Modal :openModal='addActive' @closeRequest='close'></Modal>

      <button class="button is-large is-rounded is-inverted is-light" @click="openModal">SIGN IN</button>

    </div>
  </main>
</template>


<script>
import Modal from './Modal'
import db from './firebaseInit'


export default {
  name: 'landing-page',
  components: {
    Modal
  },

  data() {
    return {
      addActive: ''
    }
  },

  methods: {
    openModal() {
      this.addActive = 'is-active';
    },

    close() {
      this.addActive = ''
    },

    open(link) {
      this.$electron.shell.openExternal(link)
    },
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

main {
  display: flex;
  justify-content: space-between;
  font-family: 'Source Sans Pro', sans-serif;
}

main>div {
  flex-basis: 100%;
}

#image {
  border-radius: 4px;
  border: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vh;
  background-color: black;
}

#image:before {
  border-radius: 4px;
  border: 0;
  display: inline-block;
  position: relative;
  -moz-pointer-events: none;
  -webkit-pointer-events: none;
  -ms-pointer-events: none;
  pointer-events: none;
  background-image: url("../assets/bg.jpg");
  height: 100vh;
  width: 100vw;
  opacity: 0.5;
  background-size: cover;
  background-position: center;
  content: '';
  left: 0;
  top: 0;
  position: absolute;
}

</style>
