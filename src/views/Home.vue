<template>
  <div >
    <button-cmp :to="{ name: 'page' }" />
    <button-cmp :to="{ name: 'page' }" theme="success" />
    <button-cmp :to="{ name: 'page' }" theme="success" size="large" />

    <button-cmp @click.prevent="clicked"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ButtonCmp from '@/components/basic/ButtonCmp'

export default {
  name: 'home',
  components: {
    ButtonCmp
  },
  methods: {
    clicked() {
      console.log('CLICKED')
    }
  }
}
</script>

