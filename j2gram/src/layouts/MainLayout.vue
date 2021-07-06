<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title >
          J2GRAM
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-footer reveal class="bg-white">
          <q-tabs class="text-grey-9" active-color="light-blue-6" indicator-color="transparent">
            <q-route-tab to="/" name="mails" :icon="$q.platform.is.ios ? 'eva-home-outline':'home'" label="Home" />
            <q-route-tab to="/camera" name="alarms" icon="photo_camera" label="Camera" />
          </q-tabs>
      </q-footer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  data () {
    return {
    }
  }
}
</script>
