<template>
  <q-page>
<h2 class="text-amber text-center"> Entre em contato com a gente! </h2>
<p class="text-h5 text-center">As mensagens serão respondidas o quanto antes possível pela nossa equipe, por favor tire qualquer dúvida por meio do formulário abaixo</p>
<div class="q-pa-md q-my-xl" style="max-width: 500px">

    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
      <q-input
        filled
        v-model="name"
        label="Seu nome completo *"
        hint="Nome e sobrenome"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Por favor digite algo.']"
      />

      <q-input
        filled
        type="number"
        v-model="age"
        label="Sua idade *"
        lazy-rules
        :rules="[
          val => val !== null && val !== '' || 'Por favor digite sua idade.',
          val => val > 0 && val < 100 || 'Por favor digite sua idade verdadeira.'
        ]"
      />

<q-input
        v-model="textareaModel"
        filled
        clearable
        type="textarea"
        color="amber"
        label="Digite sua mensagem"
        :shadow-text="textareaShadowText"
        @keydown="processTextareaFill"
        @focus="processTextareaFill"
      />
      <div>
        <q-btn label="Enviar" type="submit" color="amber"/>
        <q-btn label="Apagar" type="reset" color="amber" flat class="q-ml-sm" />
      </div>
    </q-form>

  </div>
  </q-page>
</template>
<script>
export default {
  name: 'PageContato',
  data () {
    return {
      name: null,
      age: null,
      textarea: null,

      accept: false
    }
  },

  methods: {
    onSubmit () {
      if (this.accept !== true) {
        this.$q.notify({
          color: 'red-5',
          textColor: 'white',
          icon: 'warning',
          message: 'You need to accept the license and terms first'
        })
      } else {
        this.$q.notify({
          color: 'green-4',
          textColor: 'white',
          icon: 'cloud_done',
          message: 'Submitted'
        })
      }
    },

    onReset () {
      this.name = null
      this.age = null
      this.accept = false
    }
  }
}
</script>
<style>
</style>
