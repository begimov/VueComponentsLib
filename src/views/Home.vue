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

    <p>
      <form-label-cmp for="textarea">Text:</form-label-cmp>
      <text-area-cmp name="textarea" v-model="form.text" placeholder="Enter message..." />
    </p>

    <p>
      <modal-cmp />
    </p>
  </div>
</template>

<script>
// @ is an alias to /src
import ButtonCmp from '@/components/basic/ButtonCmp'
import InputCmp from '@/components/basic/InputCmp'
import FormLabelCmp from '@/components/basic/FormLabelCmp'
import TextAreaCmp from '@/components/basic/TextAreaCmp'
import ModalCmp from '@/components/basic/ModalCmp'

export default {
  name: 'home',
  data () {
    return {
      form: {
        password: '',
        text: ''
      }
    }
  },
  components: {
    ButtonCmp,
    InputCmp,
    FormLabelCmp,
    TextAreaCmp,
    ModalCmp
  },
  methods: {
    clicked() {
      console.log('CLICKED')
    }
  }
}
</script>

