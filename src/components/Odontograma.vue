<template>
  <div class="">

    <ul>
      <li v-for="pieza in piezas">
        <div class="pieza_completa">
          <div class="cara-pieza" :class="`cara-pieza__${prueba}`" v-for="prueba in pieza" role="button">{{prueba}}</div>
        </div>
      </li>
    </ul>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        piezas: []
      }
    },

    created() {
      this.crear_piezas();
    },

    methods: {
      crear_piezas() {
        let arreglo = Array.from(Array(5).keys())
          .map(element => {
            return Array.from(Array(5).keys())
          })
        this.piezas = arreglo
      }
    }
  }
</script>

<style scoped>
  .pieza_completa {
    /*-webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    transform: rotate(45deg);*/
    -webkit-transition: box-shadow .3s ease-in-out;
    -moz-transition: box-shadow .3s ease-in-out;
    transition: box-shadow .3s ease-in-out;
    position: relative;
    border: 2px solid #b5b5b5;
    border-radius: 250%;
    width: 80px;
    height: 80px;
    overflow: hidden;
    font-size: 0;
    box-sizing: content-box;
  }

  li {
    display: inline-block;
    box-sizing: content-box;



  }

  .cara-pieza {
    display: inline-block;
    box-sizing: content-box;
    border: 1px solid #b5b5b5;
    background-color: #fff;
    width: 38px;
    height: 38px;
  }

  .cara-pieza:hover {
    background-color: red;
  }

  .cara-pieza__0,
  .cara-pieza__1 {
    border-top: 1px solid #fff !important;
  }

  .cara-pieza__0,
  .cara-pieza__2 {
    border-left: 1px solid #fff !important;
  }

  .cara-pieza__1,
  .cara-pieza__3 {
    border-right: 1px solid #fff !important;
  }

  .cara-pieza__2,
  .cara-pieza__3 {
    border-bottom: 1px solid #fff !important;
  }

  .cara-pieza__4 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 50%;
  }
</style>