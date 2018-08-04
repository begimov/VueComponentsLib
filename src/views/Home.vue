<template>
  <div >
    <button-cmp  :to="{ name: 'page' }" />
  </div>
</template>

<script>
// @ is an alias to /src
import ButtonCmp from '@/components/basic/ButtonCmp'

export default {
  name: 'home',
  components: {
    ButtonCmp
  }
}
</script>

