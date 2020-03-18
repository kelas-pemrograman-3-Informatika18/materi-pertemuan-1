<template>
  <q-page>
    Halaman Login
    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-gutter-md"
    >
      <q-input
        filled
        v-model="username"
        label="Username Anda"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Tolong Ketik Username']"
      />

      <q-input
        filled
        type="password"
        v-model="password"
        label="Password Anda"
        lazy-rules
        :rules="[
          val => val !== null && val.length > 0 || 'Password Tidak Boleh Kosong'
        ]"
      />
      <div>
        <q-btn label="Submit" type="submit" color="primary"/>
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>
  </q-page>
</template>
<script>
export default {
  data () {
    return {
      username: null,
      password: null
    }
  },
  methods: {
    onSubmit () {
      console.log('Ini fungsi Submit')
    },
    onReset () {
      console.log('Ini fungsi Reset')
    }
  }
}
</script>
