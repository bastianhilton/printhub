<template>
  <div>
    <categories />
    <!-- Footer -->
    <footer class="bg-light text-center ">
      <!-- Grid container -->
      <div class="container p-4">
      </div>
      <!-- Grid container -->

      <!-- Copyright -->
      <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2)">
        @ {{ new Date().getFullYear() }} — Copyright:
        <a class="text-dark" href="/">PrinterHub</a>
      </div>
      <!-- Copyright -->

    </footer>
    <!-- Footer -->
  </div>
</template>

<script>
  import categories from '~/components/Printers/categories'

  export default {
    components: {
      categories
    },
    name: 'IndexPage'
  }

</script>
