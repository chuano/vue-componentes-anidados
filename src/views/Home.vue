<template>
  <user-profile
    :user="user"
    class="border-red padding"
  >
  </user-profile>
</template>

<script>
import UserProfile from '@/components/UserProfile'

export default {
  name: 'Home',
  data() {
    return {
      user: null
    }
  },
  created() {
    this.getUser();
  },
  methods: {
    getUser() {
      this.user = {
        name: 'Name',
        lastname: 'Lastname',
        address: [
          {
            address: 'Address',
            zipCode: '03640',
            mainAddress: true
          },
          {
            address: 'Address 2',
            zipCode: '03640',
            mainAddress: false
          }
        ]
      };
    }
  },
  components: {
    UserProfile
  }
}
</script>