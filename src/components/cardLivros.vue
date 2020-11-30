<template>
    <div class="row align-center justify-around">
      <div class="col-md-3 q-ma-lg q-mt-xl" v-for="book in books" :key="book.id" >
          <q-card class="my-card text-blue-10">
            <q-card-section>
                <div class="txt-preco text-h6 ">R${{book.preco}}</div>
                <div class="text-h5">{{book.nome}}</div>
                <div class="text-subtitle2">autor {{book.autor}}</div>
            </q-card-section>
            <q-card-section>
                {{ book.descricao }}
            </q-card-section>

            <q-card-actions>
                <q-btn flat class="justify-flex-end" to="/editar">Editar</q-btn>
            </q-card-actions>
            
        </q-card> 
      </div>
    </div>
   
</template>

<script>
export default {
    name:'cardLivros',
    data () {
        return {
            books:[
                {
                    id:1,
                    descricao: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                    nome:'Nome Livro',
                    autor:'Jhon Doe',
                    preco:'15,00'
                },
                {
                     id:2,
                    descricao: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                    nome:'Nome Livro',
                    autor:'Jhon Doe',
                    preco:'15,00'
                },
                 {
                    id:3,
                    descricao: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
                    nome:'Nome Livro',
                    autor:'Jhon Doe',
                    preco:'15,00'
                },

            ]
        }   
  }
}
</script>

<style>
    .my-card{
        background-color: #A6DAE8;
        
   }
   .txt-preco{
       display: flex;
       float: right;
   }
</style>
