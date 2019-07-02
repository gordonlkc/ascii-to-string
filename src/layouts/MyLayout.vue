<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          ASCII to STRING
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal elevated>
      <q-toolbar>
        <q-toolbar-title>Powered by
          <a href='me.gordonlam.space' class='text-white'><u>Gordon Lam</u>
          </a>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar';

export default {
  name: 'MyLayout',
  data() {
    return {
      leftDrawerOpen: this.$q.platform.is.desktop,
    };
  },
  methods: {
    openURL,
  },
};
</script>

<style>
</style>
