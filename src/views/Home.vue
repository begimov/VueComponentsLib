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
      <input-cmp type="password" name="password" />
    </p>
  </div>
</template>

<script>
// @ is an alias to /src
import ButtonCmp from '@/components/basic/ButtonCmp'
import InputCmp from '@/components/basic/InputCmp'

export default {
  name: 'home',
  components: {
    ButtonCmp,
    InputCmp
  },
  methods: {
    clicked() {
      console.log('CLICKED')
    }
  }
}
</script>

