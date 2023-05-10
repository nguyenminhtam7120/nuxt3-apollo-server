<template>
  <div>
    <h3>List product:</h3>
    <div v-for="(item, idx) in result?.products" :key="idx">
      <p>{{ idx + 1 }}: {{ item.title }}</p>
    </div>
    <br>
    <h3>Actions</h3>
  </div>
</template>

<script lang="ts" setup>
const query = gql`
query {
  products {
    title
    description
  }
}
`
const { result } = useQuery(query);

</script>
