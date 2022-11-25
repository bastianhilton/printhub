<template>
  <div>
    <!-- Container for demo purpose -->
    <div class="container my-5 py-5">

      <!-- Section: Design Block -->
      <section class="mb-10">

        <div class="card mb-3">
          <div class="row g-0 d-flex align-items-center">
            <div class="col-lg-4 d-none d-lg-flex">
              <img src="https://mdbootstrap.com/img/new/ecommerce/vertical/126.jpg" alt="Trendy Pants and Shoes"
                class="w-100 rounded-t-5 rounded-tr-lg-0 rounded-bl-lg-5" />
            </div>
            <div class="col-lg-8">
              <div class="card-body py-5 px-md-5">
                <h2 class="fw-bold mb-4">Printer Name</h2>
                <p class="text-muted mb-4">
                  Printer Description
                </p>

                <div class="row mb-3">
                  <div class="col-lg-4 mb-2">
                    <p>
                      <i class="fas fa-check-circle text-dark me-2"></i>Function<br>
                      <i></i>
                    </p>
                  </div>

                  <div class="col-lg-4 mb-2">
                    <p>
                      <i class="fas fa-check-circle text-dark me-2"></i>MAC Address<br>
                      <i></i>
                    </p>
                  </div>

                  <div class="col-lg-4 mb-2">
                    <p>
                      <i class="fas fa-check-circle text-dark me-2"></i>IP Address<br>
                      <i></i>
                    </p>
                  </div>
                  <div class="col-lg-4 mb-2">
                    <p>
                      <i class="fas fa-check-circle text-dark me-2"></i>FQDN<br>
                      <i></i>
                    </p>
                  </div>

                  <div class="col-lg-4 mb-2">
                    <p>
                      <i class="fas fa-check-circle text-dark me-2"></i>Subnet<br>
                      <i></i>
                    </p>
                  </div>

                  <div class="col-lg-4 mb-2">
                    <p>
                      <i class="fas fa-check-circle text-dark me-2"></i>Printer Status<br>
                      <i></i>Active
                    </p>
                  </div>
                </div>

                <button type="button" class="btn btn-dark btn-lg px-5">
                  <!--<a :href="`/create/${printer.id}`">Edit</a>-->
                </button>
              </div>
            </div>
          </div>
          <div class="container my-5">

            <hr class="my-5" />

            <!--Section: Printer Details--------------------------------------------------------->
            <section>

              <div class="row">
                <div class="col-lg-6 mb-4 mb-lg-0 pb-2 pb-lg-0 pb-xl-2">
                  <h5 class="text-uppercase mb-5">Printer Details</h5>
                  <figure class="border-left border-primary ps-3 py-2 mb-4">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>WHID
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">July, 2013 - Present (4 years)</p>
                      <p class="mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2 mb-4">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Driver
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2011 - June 2012 (1 year, 3 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum quas, eos
                        officia maiores ipsam ipsum dolores.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Printer Location
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Default Papersize
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Duplex Option
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Last Permission Update
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                </div>
                <!-- Right Side of Printer Details -->
                <div class="col-lg-6 mb-4 mb-lg-0 pb-2 pb-lg-0 pb-xl-2">
                  <h5 class="text-uppercase mb-5"></h5>
                  <figure class="border-left border-primary ps-3 py-2 mb-4">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Applied Permissions
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">July, 2013 - Present (4 years)</p>
                      <p class="mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2 mb-4">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Color Option
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2011 - June 2012 (1 year, 3 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laborum quas, eos
                        officia maiores ipsam ipsum dolores.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Default Tray
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Last Driver Update
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Last Settings Update
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                  <figure class="border-left border-primary ps-3 py-2">
                    <blockquote class="blockquote">
                      <h5 class="pb-3">
                        <i class="fas fa-briefcase me-3" aria-hidden="true"></i>Last Location Update
                      </h5>
                    </blockquote>
                    <figcaption class="blockquote-footer mb-0">
                      <p class="font-weight-bold text-body mb-2">
                        March 2005 - May 2011 (6 years, 2 Month)
                      </p>
                      <p class="mb-0">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit integer posuere.
                      </p>
                    </figcaption>
                  </figure>
                </div>
              </div>
            </section>
            <!--Section: Design Block-->

            <hr class="my-5" />

            
          </div>

          <div class="container my-5">
            <!--Section: Design Block-->
            <section>
              <h3 class="text-center mb-5">Printer Images</h3>
              <div class="lightbox">
                <div class="row">
                  <div class="col-md-4 mb-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Thumbnail/img%20(63).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Thumbnail/img%20(63).jpg"
                      alt="Lightbox image 1" class="w-100 shadow-1-strong rounded" />
                  </div>
                  <div class="col-md-4 mb-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(66).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(66).jpg"
                      alt="Lightbox image 2" class="w-100 shadow-1-strong rounded" />
                  </div>
                  <div class="col-md-4 mb-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(65).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(65).jpg"
                      alt="Lightbox image 3" class="w-100 shadow-1-strong rounded" />
                  </div>
                </div>
                <div class="row">
                  <div class="col-md-4 mb-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(67).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(67).jpg"
                      alt="Lightbox image 4" class="w-100 shadow-1-strong rounded" />
                  </div>
                  <div class="col-md-4 mb-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(68).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(68).jpg"
                      alt="Lightbox image 5" class="w-100 shadow-1-strong rounded" />
                  </div>
                  <div class="col-md-4 mb-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(64).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(64).jpg"
                      alt="Lightbox image 6" class="w-100 shadow-1-strong rounded" />
                  </div>
                </div>
                <div class="row">
                  <div class="col-md-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(69).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(69).jpg"
                      alt="Lightbox image 7" class="w-100 shadow-1-strong rounded" />
                  </div>
                  <div class="col-md-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(59).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(59).jpg"
                      alt="Lightbox image 8" class="w-100 shadow-1-strong rounded" />
                  </div>
                  <div class="col-md-4">
                    <img src="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(70).jpg"
                      data-mdb-img="https://mdbootstrap.com/img/Mockups/Lightbox/Original/img%20(70).jpg"
                      alt="Lightbox image 9" class="w-100 shadow-1-strong rounded" />
                  </div>
                </div>
              </div>
            </section>
            <!--Section: Design Block-->
          </div>
        </div>
      </section>
      <!-- Section: Design Block -->

    </div>
    <!-- Container for demo purpose -->
    <related />
  </div>
</template>

<script>
  import related from '~/components/Printers/related'

  export default {
    components: {
      related
    },
    head: {
      title: 'Printer'
    }
  }

</script>

<style>
  .rounded-t-5 {
    border-top-left-radius: 0.5rem;
    border-top-right-radius: 0.5rem;
  }

  @media (min-width: 992px) {
    .rounded-tr-lg-0 {
      border-top-right-radius: 0;
    }

    .rounded-bl-lg-5 {
      border-bottom-left-radius: 0.5rem;
    }
  }

  .nav-pills .nav-link.active,
  .nav-pills .nav-item.show .nav-link {
    background-color: #4f66a7;
    color: #fff;
  }

  .card.hover-shadow-light,
  .hover-shadow-light {
    transition: all 0.5s ease-in-out;
  }

  .card.hover-shadow-light:hover,
  .hover-shadow-light:hover {
    box-shadow: 0 8px 17px 0 rgba(0, 0, 0, 0.05), 0 6px 20px 0 rgba(0, 0, 0, 0.05);
    transition: all 0.5s ease-in-out;
  }

  .blockquote-footer:before {
    content: none;
  }

  .border-left {
    border-left: 3px solid #facc62 !important;
  }

</style>
