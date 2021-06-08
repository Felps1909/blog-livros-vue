<template>
	<div class="cadastro">
		<form>
			<p class="text-h4 text-white text-center">Cadastro</p>
			<q-input
			 color="white" label-color="white" 
			 type="text" v-model="nome" label="Nome Usuario"
			 :rules="[val =>  !!val && val.length >= 6 || 'Preencha o Campo com no minimo 6 caracteres']"/>
			<q-input 
			  
			  color="white" 
				label-color="white" 
				v-model="email"  type="email" label="Email" 
				:rules="[ val => !!val || 'Preencha o campo!']"/>
			<q-input
			 
			 color="white" label-color="white"  
			 v-model="password" :type="isPwd ? 'password' : 'text'"
			  label="Senha"
				:rules="[ val =>  !!val && val.length >= 6 || 'Preencha o Campo com no minimo 6 caracteres']"
			/>
			<q-input 
			 class="q-mb-lg"
				v-model="password" 
				:type="isPwd ? 'password' : 'text'"
				label="Confirme Senha"
				color="white" label-color="white"
			
			>
        <template v-slot:append>
          <q-icon
            :name="isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="isPwd = !isPwd"
          />
        </template>
      </q-input>
			<q-btn class="btn" color="red-4" text-color="white" label="Enviar" />
			<q-btn class="btn" color="red-4" text-color="white" label="Limpar" @click="reset"/>
		</form>
	</div>		
</template>
<script>
export default {
	name:'Cadastro',
	data () {
		return{
			password: null,
      isPwd: true,
			email: null,
			nome:null
		}
	},
	methods:{
		reset(){
			Object.assign(this.$data, this.$options.data());
		}
	}
}
</script>
<style>

</style>


