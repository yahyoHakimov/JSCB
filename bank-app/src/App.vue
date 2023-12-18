<script>
import AccountInfo from '@/AccountInfo.vue'

export default {
  components: {AccountInfo},
  data () {
    return {
      userData: ''
    }
  },
  created() {
    fetch()
        .then(res => res.json())
        .then(data => { this.userData = data})
        .catch(error => console.log('Error fetching API: ', error));
  },

}
</script>

<template>
  <AccountInfo :user="userData"/>
</template>