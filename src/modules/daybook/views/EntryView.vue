<template>
  <div class="entry-title d-flex justify-content-between p-2">
    <div>
        <span class="text-success fs-3 fw-bold">15</span>
        <span class="mx-1 fs-3">Julio</span>
        <span class="mx-2 fs-4 fw-light">2022, Sabado</span>
    </div>
    <div>
      <buton class="btn btn-danger mx-2">
        Borrar
        <i class="fa fa-trash-alt"></i>
      </buton>
      <buton class="btn btn-primary">
        Subir Foto
        <i class="fa fa-upload"></i>
      </buton>
    </div>
  </div>
  <hr>
  <div class="d-flex flex-column px-3 h-75">
    <textarea placeholder="Que sucedio hoy?"></textarea>
  </div>
  <FabComponent icono="fa-save"/>
  <img src="https://compass-ssl.xbox.com/assets/9c/94/9c944d9c-7ef1-4b46-9f68-9b02966d3993.jpg?n=Halo-Infinite_GLP-Page-Hero-0_1083x609.jpg" 
  alt="entry-picture" class="img-thumbnail">
</template>

<script>
import { defineAsyncComponent } from '@vue/runtime-core'
export default {
  components:{
    FabComponent: defineAsyncComponent(() => import('../components/FabComponent'))
  }

}
</script>

<style lang="scss" scoped>
textarea{
  font-size: 20px;
  border: none;
  height: 100%;

  &:focus{
    outline: none;
  }
}
img{
  width: 200px;
  position: fixed;
  bottom: 150px;
  right: 20px;
  box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
}
</style>