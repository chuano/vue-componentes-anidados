<template>
  <div>
    <h1 class="red">User profile</h1>
    <p>Name: {{ user.name }}</p>
    <p>Lastname: {{ user.lastname }}</p>
    <address-list
      :address="user.address"
      class="border-green padding"
    >
    </address-list>
  </div>
</template>

<script>
import AddressList from '@/components/Address/AddressList'

export default {
  name: 'UserProfile',
  props: {
    user: {
      default: null
    }
  },
  components: {
    AddressList
  }
}
</script>