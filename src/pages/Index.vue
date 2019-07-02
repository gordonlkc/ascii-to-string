<template>
  <q-page class='flex flex-center'>
    <q-layout>
      <div class="content q-pa-sm">
        <div class="row">
            <div class="col-xs-12">
              <h5>
                Please enter the ascii code.
              </h5>
            </div>
            <div class="col-xs-12">
              <q-input
                v-model="ascii"
                filled
                type="textarea"
              />
            </div>
        </div>
        <div class="row">
            <div class="col-xs-12">
              <h5>
                Please see the output.
              </h5>
            </div>
            <div class="col-xs-12">
              <q-input
                v-model="string"
                filled
                type="textarea"
                readonly
              />
            </div>
        </div>
      </div>
    </q-layout>
  </q-page>
</template>

<style>
.completed-line {
  text-decoration: line-through;
}
</style>

<script>

export default {
  name: 'PageIndex',
  data() {
    return {
      ascii: '119 097 110 110 097 032 098 101 032 119 105 116 104 032 121 111 117',
      string: '',
    };
  },
  methods: {
  },
  watch: {
    ascii: {
      handler(val) {
        const codes = val.split(' ');
        this.string = ''; // clean the existing
        codes.forEach((code) => {
          this.string = this.string + (String.fromCharCode(code));
        });
      },
      immediate: true,
    },
  },
};
</script>
