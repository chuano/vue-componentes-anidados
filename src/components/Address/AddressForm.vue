<template>
  <div>
    <h2 class="orange">New address</h2>
    <form @submit.prevent="submit()">
      <div>
        <input type="text" v-model="address" placeholder="Address"/>
      </div>
      <div>
        <input type="text" v-model="zipCode" placeholder="ZIP Code"/>
      </div>
      <div>
        <select v-model="mainAddress">
          <option :value="false">No</option>
          <option :value="true">Yes</option>
        </select>
      </div>
      <div>
        <button type="submit">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'AddressForm',
  data() {
    return {
      address: null,
      zipCode: null,
      mainAddress: false
    }
  },
  methods: {
    submit() {
      this.$emit('submit', {
        address: this.address,
        zipCode: this.zipCode,
        mainAddress: this.mainAddress
      });
      this.address = null;
      this.zipCode = null;
      this.mainAddress = false;
    }
  }
}
</script>