<script>
  import CustomerRow from "./CustomerRow.svelte";
  // when we imported CustomerRow.svelte, as described in
  // CustomerRow.svelte, we will be able to use the
  // CustomerRow component in this file, and pass it a
  // `customers` prop
  export let customers;
</script>

<table>
  <thead>
    <tr>
      <th>ID</th>
      <th>First name</th>
      <th>Last name</th>
      <th>Email address</th>
    </tr>
  </thead>
  <tbody>
    {#each customers as customer (customer.id)}
      <CustomerRow {customer} />
    {/each}
  </tbody>
</table>

<style>
  table {
    width: 100%;
    text-align: left;
    border-collapse: collapse;
  }

  tr {
    background-color: rgb(42, 139, 70);
    color: white;
  }

  th {
    padding: 10px;
    padding-right: 0;
  }
</style>
