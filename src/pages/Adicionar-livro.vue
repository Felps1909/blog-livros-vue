<template>
    <q-page>
        <navbar/>
        <div>
			<q-btn class="botao text-blue-10 q-ma-sm"   label="Voltar" to="/livros"/>
		</div>
		<div class="row align-center justify-around">
			<div class=" content-cad-livro col-md-8 col-sm-6 text-center  text-blue-10 ">
				<h4 class="q-mt-md">Cadastro de Livros</h4>
				<q-form class="q-ma-lg  ">
					<q-input
					class="campo"
					color="white" 
					label-color="blue-10" 
					v-model="nomeLivro"
					label="Nome do livro"
					lazy-rules
					:rules="[ val => val && val.length > 0 || 'Campo Obrigatório *']"
					>
					
					</q-input>
					<q-input 
					class="campo" 
					v-model="preco"
					prefix="$"
					label="Preço"
					color="white"
					label-color="blue-10"
					mask="#.##"
					fill-mask="0"
					reverse-fill-mask
					lazy-rules
					:rules="[ val => val && val.length > 0 || 'Campo Obrigatório *']"
					>
					</q-input>
					<q-input
					class="campo"
					color="white" 
					label-color="blue-10" 
					v-model="categoria"
					label="Categoria"
					lazy-rules
					:rules="[ val => val && val.length > 0 || 'Campo Obrigatório *']"
					>
					</q-input>
					<q-input
					class="campo q-mb-md"
					color="white" 
					label-color="blue-10" 
					v-model="subCategoria"
					label="Subcategoria"
					
					>
					</q-input>
					<q-btn class="btn q-mr-sm " color="red-5" text-color="white" label="Cadastrar" />
					<q-btn class="btn " color="red-5" text-color="white" label="Limpar" @click="reset"/>
				</q-form>
			</div>
		</div>
    </q-page>
</template>

<script>
import navbar from '../components/navBar'
export default {
	data(){
		return{
			nomeLivro:'',
			preco:'',
			Categoria:'',
			subCategoria:''
		}
	},
    components:{
        navbar
       
	},
	methods:{
		reset(){
			Object.assign(this.$data, this.$options.data());
		}
	}
}
</script>

<style>
    *{
        padding: 0;
        margin: 0;
    }
	.content-cad-livro{
		background-color: #A6DAE8;
	}
	.botao{
		background-color: #A6DAE8;
	}
	.campo input{
		color: red
		;
	}
	/* .content{
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	} */
</style>