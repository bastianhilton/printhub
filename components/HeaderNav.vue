<template>
  <header>
    <!-- Sidenav -->
    <nav id="sidenav-1" class="sidenav bg-primary" data-mdb-hidden="true">
      <ul class="sidenav-menu">
        <li class="sidenav-item">
          <a class="sidenav-link"  href="/">
            <i class="fas fa-home fa-fw me-3" style="color: white;"></i><span>Home</span></a>
        </li>
        <li class="sidenav-item">
          <a class="sidenav-link" style="color: white;" href="/siteprinters">
            <i class="fas fa-table fa-fw me-3" style="color: white;"></i><span>Data by WHID</span></a>
        </li>
        <li class="sidenav-item">
          <a class="sidenav-link" style="color: white;" href="/logs">
            <i class="fas fa-database fa-fw me-3" style="color: white;"></i><span>View BODP Logs</span></a>
        </li>
        <li class="sidenav-item">
          <a class="sidenav-link" style="color: white;" href="/fleet">
            <i class="fas fa-chart-pie fa-fw me-3" style="color: white;"></i><span>Fleet Browser</span></a>
        </li>
        <li class="sidenav-item">
          <a class="sidenav-link" style="color: white;" href="/metrics">
            <i class="fas fa-chart-area fa-fw me-3" style="color: white;"></i><span>Metrics</span></a>
        </li>
        <li class="sidenav-item">
          <a class="sidenav-link" style="color: white;" href="https://t.corp.amazon.com">
            <i class="fas fa-ticket-alt fa-fw me-3" style="color: white;"></i><span>Create A Ticket</span></a>
        </li>
        <li class="sidenav-item">
          <a class="sidenav-link" style="color: white;" href="/about">
            <i class="fas fa-at fa-fw me-3" style="color: white;"></i><span>About Us</span></a>
        </li>
      </ul>
    </nav>
    <!-- Sidenav -->

    <!-- Navbar -->
    <nav id="main-navbar" class="navbar navbar-expand-lg navbar-light bg-primary fixed-top" style="z-index:999999">
      <!-- Container wrapper -->
      <div class="container-fluid">
        <!-- Toggler -->
        <button data-mdb-toggle="sidenav" data-mdb-target="#sidenav-1" class="btn btn-primary"
          aria-controls="#sidenav-1" aria-haspopup="true">
          <i class="fas fa-bars"> Menu</i>
        </button>
        <a class="navbar-brand" href="/">
          <div class="metroname" style="color:orange;">Printer</div>
          <div class="metroname" style="color:powderblue;">Hub</div>
        </a>
        <!-- Search form -->
        <div class="collapse navbar-collapse justify-content-center" id="navbarCenteredExample">
          <MainSearch />
        </div>

        <ul class="navbar-nav ms-auto d-flex flex-row">
         <li class="nav-item dropdown">
            <a class="nav-link me-3 me-lg-0 dropdown-toggle hidden-arrow" href="#" id="navbarDropdownMenuLink"
              role="button" data-mdb-toggle="dropdown" aria-expanded="false">
              Add New
              <span class="badge rounded-pill badge-notification bg-danger"></span>
            </a>
            <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdownMenuLink">
              <li><a class="dropdown-item" href="/create/printer">Add A Printer</a></li>
              <li><a class="dropdown-item" href="/create/site">Add A Site</a></li>
            </ul>
          </li>

          <!-- Avatar -->
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle hidden-arrow d-flex align-items-center" href="#"
              id="navbarDropdownMenuLink" role="button" data-mdb-toggle="dropdown" aria-expanded="false">
              <img src="../static/images/mbr-1.png" class="rounded-circle" height="22"
                alt="" loading="lazy" />
            </a>
            <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdownMenuLink">
              <li>
                <a class="dropdown-item" target="_blank" href="/myprinters">My Printers</a>
              </li>
              <li>
                <a class="dropdown-item" aria-current="page" @click.prevent="handleLogout">Logout</a>
              </li>
            </ul>
          </li>
        </ul>
      </div>
      <!-- Container wrapper -->
    </nav>
    <!-- Navbar -->
  </header>
</template>

<script>
import MainSearch from '~/components/MainSearch.vue'
// import { mapGetters } from 'vuex'

export default {
    components: {
      MainSearch,
    },
}
</script>

<style>

</style>
