<template>
	<div class="Login">
		<form class="q-mt-sm">
			<p class="text-h4 text-white text-center">Entrar</p>
			<q-input 
			  color="white" 
				label-color="white" 
				v-model="email"  type="email" label="Email"  
				:rules="[val => !!val || 'Preencha o campo!']"/>
			<q-input 
			 class="q-mb-lg"
				v-model="password" 
				:type="isPwd ? 'password' : 'text'"
				label="Senha"
				color="white" label-color="white"
				:rules="[val => !!val || 'Preencha o campo!']"
			>
        <template v-slot:append>
          <q-icon
            :name="isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="isPwd = !isPwd"
          />
        </template>
      </q-input>
			<q-btn class="btn" color="red-4" text-color="white" label="Entrar" />
			<q-btn class="btn" color="red-4" text-color="white" label="Limpar" @click="reset" />
		</form>
	</div>
</template>
<script>
export default {
	name:'Login',
	data () {
    return {
			email:null,
			password: null,
			isPwd: true
    }
	},
	methods:{
		reset (){
			Object.assign(this.$data, this.$options.data());
		}
	}
}
</script>
<style>
	input[label]{
		color: blue
	}
	.btn{
		margin: 0.5rem 0.8rem;
		width: 10vw;

	}
</style>

