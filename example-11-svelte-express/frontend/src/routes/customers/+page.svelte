<script>
  import CustomerTable from "$lib/components/CustomerTable.svelte";

  /**
   * Define a special prop called "data", which will be automatically filled by SvelteKit, with the result
   * of running the load() function defined in +page.js.
   */
  export let data;

  // The flow of data is:
  // 1. SvelteKit calls the load() function in +page.js
  // 2. data return from load() is passed to the +page.svelte
  //    as the `data` prop
  // 3. The `data` prop is passed to the CustomerTable component
  //   as the `customers` prop
  // 4. The CustomerTable component uses the `customers` prop
  //   and supplies it to the CustomerRow component as the `customer` prop
</script>

<h1>Customers</h1>

<!-- Display customer data in a table component. -->
<CustomerTable customers={data.customers} />
