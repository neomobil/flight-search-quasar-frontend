<template>
  <div class="row q-col-gutter-md">
    <div class="col-xs-12 col-sm-6 col-md-4 offset-md-2">
      <q-input v-model="form.o1" outlined label="First origin" error-message="bu" :error="false" dense/>
      <q-input v-model="form.dd1" outlined mask="date" :rules="['date']" label="Date" dense>
        <template v-slot:append>
          <q-icon name="event" class="cursor-pointer">
            <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">
              <q-date v-model="form.dd1" @input="() => $refs.qDateProxy.hide()"/>
            </q-popup-proxy>
          </q-icon>
        </template>
      </q-input>
      <q-input v-model="form.d1" outlined label="First destination" error-message="bu" :error="false" dense/>
    </div>
    <div class="col-xs-12 col-sm-6 col-md-4">
      <q-input v-model="form.o2" outlined label="Second origin" error-message="bu" :error="false" dense/>
      <q-input v-model="form.dd2" outlined mask="date" :rules="['date']" label="Date" dense>
        <template v-slot:append>
          <q-icon name="event" class="cursor-pointer">
            <q-popup-proxy ref="qDateProxy2" transition-show="scale" transition-hide="scale">
              <q-date v-model="form.dd2" @input="() => $refs.qDateProxy2.hide()"/>
            </q-popup-proxy>
          </q-icon>
        </template>
      </q-input>
      <q-input v-model="form.d1" outlined label="Second destination" error-message="bu" :error="false" dense/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchForm',
  data () {
    return {
      form: {
        d1: null,
        d2: null,
        o1: null,
        o2: null,
        dd1: null,
        dd2: null
      }
    }
  }
}
</script>
