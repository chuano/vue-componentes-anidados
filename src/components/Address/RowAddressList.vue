<template>
  <div>
    <h3 class="blue">Address</h3>
    <p>Address: {{ address.address }}</p>
    <p>ZIP Code: {{ address.zipCode }}</p>
    <p>Main address: {{ address.mainAddress ? 'Yes' : 'No' }}</p>
  </div>
</template>

<script>
export default {
  props: {
    address: {
      default: null
    }
  }
}
</script>