<template>
  <div>
    <h2 class="green">User address list</h2>
    <address-form
      @submit="addAddress($event)"
      class="border-orange padding"
    ></address-form>
    <row-address-list
      v-for="(addr, index) in address"
      :key="index"
      :address="addr"
      class="border-blue padding"
    >
    </row-address-list>
  </div>
</template>

<script>
import RowAddressList from '@/components/Address/RowAddressList'
import AddressForm from '@/components/Address/AddressForm'
export default {
  name: 'AddressList',
  props: {
    address: {
      default() {
        return []
      }
    }
  },
  methods: {
    addAddress(address) {
      this.address.push(address);
    }
  },
  components: {
    AddressForm,
    RowAddressList
  }
}
</script>