<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-amber">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
      <router-link to="/" style="text-decoration: none;"><h5 class="text-white">Instituto Aeon</h5></router-link>
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
          style="color: #EFC600"
        />
      </q-list>

      <router-link to="/" style="text-decoration: none;"><h5 class="text-amber text-center">Principal</h5></router-link>
      <router-link to="/contato" style="text-decoration: none;"><h5 class="text-amber text-center">Contato</h5></router-link>
      <router-link to="/sobre" style="text-decoration: none;"><h5 class="text-amber text-center">Sobre</h5></router-link>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="bg-grey" elevated bordered reveal>
        <q-toolbar>
          <q-toolbar-title class="text-center text-amber">Instituto Aeon - 2021 - Todos os direitos reservados ©</q-toolbar-title>
        </q-toolbar>
        <q-toolbar class="row flex items-center justify-center">
      <router-link to="/" style="text-decoration: none;" ><h5 class="q-mx-md text-primary text-center">Principal</h5></router-link>
      <router-link to="/contato" style="text-decoration: none;"><h5 class="q-mx-md text-primary text-center">Contato</h5></router-link>
      <router-link to="/sobre" style="text-decoration: none;"><h5 class="q-mx-md text-primary text-center">Sobre</h5></router-link>
      </q-toolbar>
      </q-footer>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
]

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
