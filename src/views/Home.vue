<template>
  <div >
    <p>
      <button-cmp :to="{ name: 'page' }" />
      <button-cmp :to="{ name: 'page' }" theme="success" />
      <button-cmp :to="{ name: 'page' }" theme="success" size="large" />

      <button-cmp @click.prevent="clicked"/>
      <button-cmp disabled />

      <button-cmp>PAGE</button-cmp>
    </p>

    <p>
      <form-label-cmp for="password">Password:</form-label-cmp>
      <input-cmp type="password" name="password" v-model="form.password" placeholder="Enter password..."/>
      <input-cmp name="name" />
    </p>
  </div>
</template>

<script>
// @ is an alias to /src
import ButtonCmp from '@/components/basic/ButtonCmp'
import InputCmp from '@/components/basic/InputCmp'
import FormLabelCmp from '@/components/basic/FormLabelCmp'

export default {
  name: 'home',
  data () {
    return {
      form: {
        password: ''
      }
    }
  },
  components: {
    ButtonCmp,
    InputCmp,
    FormLabelCmp
  },
  methods: {
    clicked() {
      console.log('CLICKED')
    }
  }
}
</script>

