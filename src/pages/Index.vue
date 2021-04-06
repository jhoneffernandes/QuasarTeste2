<template>
  <q-page class="flex flex-center column">
      <div class="q-pa-md">
     <div class="q-gutter y-md column">
<q-input outlined bottom-slots v-model="nome" label="Informe o nome do aluno" counter>
        <template v-slot:prepend>
          <q-icon name="person" />
        </template>
        <template v-slot:append>
          <q-icon name="close" @click="nome = ''" class="cursor-pointer" />
        </template>
      </q-input>    </div>
    </div>
      <div class="q-pa-md">
     <div class="q-gutter y-md column" style="max-width: 400px">
          <q-btn color="amber" label="Adicionar aluno" @click="adicionar" />
    </div>
    </div>
     <div class="q-pa-md">
     <div class="row column justify-center text-center items-center">
       <q-list bordered separator dense class="rounded-borders text-amber flex column justify-start text-center items-center q-my-md q-list-striped">
            <q-item clickable v-ripple class="column q-my-md" style="width: 300px" v-for="(item, index) in lista" :key="index">
                <q-item-section>
                   <h5 class="q-mx-xl">
                   <p class="text-red">Aluno(a) {{index+1}}</p>
                   <p>{{item}}</p>
                   </h5>
                </q-item-section>
                <q-item-section>
                  <q-btn @click="remover" color="red" class="q-my-sm">
                    <p class="text-white q-my-sm text-h7">Excluir Aluno<q-icon name="delete" class="q-mx-sm text-white" size="sm" /></p>
                  </q-btn>
                </q-item-section>
          </q-item>
          </q-list>
    </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      nome: '',
      lista: []
    }
  },
  methods: {
    adicionar () {
      this.lista.push(this.nome)
      this.nome = ''
    },
    remover (pos) {
      this.lista.splice(pos, 1)
    }
  }
}
</script>
