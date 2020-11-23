<template>
  <q-page class="container">
    <div class="row justify-around align-center ">
      <div class="land-page" style="max-width:320px;">
        <q-tabs
          v-model="tab"
          dense
          align="justify"
          class="bg-red-5 text-white"
          :breakpoint="0">
          <q-tab name="login" label="Login Usuario" />
          <q-tab name="cadastro" label="Registre Usuario" />
        </q-tabs>
        <q-tab-panels v-model="tab" animated>
            <q-tab-panel name="login" class="bg-red-5">
              <Login/>
            </q-tab-panel>

            <q-tab-panel name="cadastro" class="bg-red-5">
              <Cadastro/>
            </q-tab-panel>
          </q-tab-panels>
      </div>
      <img src="../assets/image-fundo.svg" class="q-mt-md" style="width:50vw;">
    </div>
  </q-page>
</template>

<script>
import Login from './Login'
import Cadastro from './Cadastro'

export default {
  name: 'PageIndex',
  components:{
    Login,
    Cadastro
  },
  data () {
    return {
      tab: 'mails'
    }
  }
}
</script>
<style>
*{
  font-family: Arial, Helvetica, sans-serif;
}
.container{
  background-color: #A6DAE8
}
.land-page{
  margin: 2rem 0
}
</style>

