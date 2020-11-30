<template>
    <header  class="bg-red-5 text-white">
        <div class="box1">
            <p>Nome Usuario</p>
        </div>
        <div class="box2">
            <p>Adicionar livro</p>
            <p>Sair</p>
        </div>
    </header>
</template>

<script>
export default {
    name:'navbar'
}
</script>

<style>
  .box1{
    width: 80vw;
    font-size: 1.5rem
  }
  .box2{
    display: flex;
    float: right;
    font-size: 1rem
  }
  .box2 p {
     padding: 0 1rem
  }
  header{
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 1rem ;
    
}
</style>
