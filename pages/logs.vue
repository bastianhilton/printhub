<template>
  <div>
    <header>
      <!-- Heading -->
      <section class="mb-5 mb-lg-8 text-center text-md-start">
        <!-- Background image -->
        <div class="p-5 bg-image" style="
              background-image: url('https://mdbootstrap.com/img/new/textures/full/66.jpg');
              height: 250px;
              "></div>
        <!-- Background image -->

        <div class="container">
          <div class="card shadow-0" style="
    margin-top: -100px;
    ">
            <div class="card-body py-5 px-5">
              <div class="row gx-lg-4 align-items-center">
                <div class="col-lg-6 mb-4 mb-lg-0 text-center text-lg-start">
                  <h1 class="">Logs Dashboard</h1>
                  <!-- Breadcrumb -->
                  <nav class="d-flex justify-content-center justify-content-lg-start">
                    <h6 class="mb-0">
                      <a href="" class="text-muted">Home</a>
                      <span>/</span>
                      <a href="" class="text-muted">Analytics</a>
                      <span>/</span>
                      <a href="" class="text-muted"><u>Logs</u></a>
                    </h6>
                  </nav>
                  <!-- Breadcrumb -->
                </div>

                <div class="col-lg-6 text-center text-lg-end">
                  <button type="button" class="btn btn-link me-1 mb-4 px-2 px-md-3" data-ripple-color="primary">
                    Customize<i class="fas fa-cogs ms-2"></i>
                  </button>
                  <button type="button" class="btn btn-link mb-4 px-2 px-md-3" data-ripple-color="primary">
                    Export<i class="fas fa-download ms-2"></i>
                  </button>

                  <div class="row justify-content-center justify-content-lg-end">
                    <div class="col-md-4 mb-4 mb-md-0">
                      <select class="select">
                        <option value="1">Today</option>
                        <option value="2">Yesterday</option>
                        <option value="3" selected>Last 7 days</option>
                        <option value="4">Last 28 days</option>
                        <option value="5">Last 90 days</option>
                      </select>
                      <label class="form-label select-label">Date</label>
                    </div>

                    <div class="col-md-4">
                      <div class="form-outline datepicker" data-mdb-inline="true">
                        <input type="text" class="form-control" id="exampleDatepicker1" data-toggle="datepicker"
                          value="Custom date" />
                        <label for="exampleDatepicker1" class="form-label">Date</label>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

            </div>
          </div>
        </div>
      </section>
      <!-- Heading -->
    </header>
    <!-- Container for demo purpose -->
    <div class="container">

      <!--Section: Summary-->
      <section>
        <div class="row gx-xl-5">
          <div class="col-lg-3 col-md-6 mb-xl-5 mb-4">
            <div class="card shadow-0">
              <div class="card-body">
                <p class="text-uppercase small mb-2">
                  <strong>USERS</strong>
                </p>
                <h5 class="mb-0">
                  <strong>14 567</strong>
                  <small class="text-success ms-2">
                    <i class="fas fa-arrow-up fa-sm pe-1"></i>13,48%</small>
                </h5>

                <hr class="hr">

                <p class="text-uppercase text-muted small mb-2">
                  Previous period
                </p>
                <h5 class="text-muted mb-0">11 467</h5>
              </div>
            </div>
            <!-- Card -->
          </div>

          <div class="col-lg-3 col-md-6 mb-xl-5 mb-4">
            <div class="card shadow-0">
              <div class="card-body">
                <p class="text-uppercase small mb-2">
                  <strong>PAGE VIEWS</strong>
                </p>
                <h5 class="mb-0">
                  <strong>51 354 </strong>
                  <small class="text-success ms-2">
                    <i class="fas fa-arrow-up fa-sm pe-1"></i>23,58%</small>
                </h5>

                <hr class="hr">

                <p class="text-uppercase text-muted small mb-2">
                  Previous period
                </p>
                <h5 class="text-muted mb-0">38 454</h5>
              </div>
            </div>
          </div>

          <div class="col-lg-3 col-md-6 mb-xl-5 mb-4">
            <div class="card shadow-0">
              <div class="card-body">
                <p class="text-uppercase small mb-2">
                  <strong>AVERAGE TIME</strong>
                </p>
                <h5 class="mb-0">
                  <strong>00:04:20</strong>
                  <small class="text-danger ms-2">
                    <i class="fas fa-arrow-down fa-sm pe-1"></i>23,58%</small>
                </h5>

                <hr class="hr">

                <p class="text-uppercase text-muted small mb-2">
                  Previous period
                </p>
                <h5 class="text-muted mb-0">00:05:20</h5>
              </div>
            </div>
          </div>

          <div class="col-lg-3 col-md-6 mb-xl-5 mb-4">
            <div class="card shadow-0">
              <div class="card-body">
                <p class="text-uppercase small mb-2">
                  <strong>BOUNCE RATE</strong>
                </p>
                <h5 class="mb-0">
                  <strong>32.35%</strong>
                  <small class="text-danger ms-2">
                    <i class="fas fa-arrow-down fa-sm pe-1"></i>23,58%</small>
                </h5>

                <hr class="hr">

                <p class="text-uppercase text-muted small mb-2">
                  Previous period
                </p>
                <h5 class="text-muted mb-0">24.35%</h5>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!--Section: Summary-->

      <!--Section: Content-->
      <section>
        <div class="row gx-xl-5">
          <div class="col-lg-9 mb-xl-5 mb-4">
            <div class="card shadow-0 h-100">
              <div class="card-body">
                <!-- Pills navs -->
                <ul class="nav nav-pills nav-justified mb-3" id="ex1" role="tablist">
                  <li class="nav-item" role="presentation">
                    <a class="nav-link active" id="ex1-tab-1" data-mdb-toggle="pill" href="#ex1-pills-1" role="tab"
                      aria-controls="ex1-pills-1" aria-selected="true">Users</a>
                  </li>
                  <li class="nav-item" role="presentation">
                    <a class="nav-link" id="ex1-tab-2" data-mdb-toggle="pill" href="#ex1-pills-2" role="tab"
                      aria-controls="ex1-pills-2" aria-selected="false">Page views</a>
                  </li>
                  <li class="nav-item" role="presentation">
                    <a class="nav-link" id="ex1-tab-3" data-mdb-toggle="pill" href="#ex1-pills-3" role="tab"
                      aria-controls="ex1-pills-3" aria-selected="false">Average time</a>
                  </li>
                  <li class="nav-item" role="presentation">
                    <a class="nav-link" id="ex1-tab-4" data-mdb-toggle="pill" href="#ex1-pills-4" role="tab"
                      aria-controls="ex1-pills-4" aria-selected="false">Bounce rate</a>
                  </li>
                </ul>
                <!-- Pills navs -->

                <!-- Pills content -->
                <div class="tab-content" id="ex1-content">
                  <div class="tab-pane fade show active" id="ex1-pills-1" role="tabpanel" aria-labelledby="ex1-tab-1">
                    <div id="chart-users"></div>
                  </div>
                  <div class="tab-pane fade" id="ex1-pills-2" role="tabpanel" aria-labelledby="ex1-tab-2">
                    <div id="chart-page-views"></div>
                  </div>
                  <div class="tab-pane fade" id="ex1-pills-3" role="tabpanel" aria-labelledby="ex1-tab-3">
                    <div id="chart-average-time"></div>
                  </div>
                  <div class="tab-pane fade" id="ex1-pills-4" role="tabpanel" aria-labelledby="ex1-tab-4">
                    <div id="chart-bounce-rate"></div>
                  </div>
                </div>
                <!-- Pills content -->
              </div>
            </div>
          </div>

          <div class="col-lg-3 mb-xl-5 mb-4">
            <div class="card shadow-0 mb-xl-5 mb-4">
              <div class="card-body">
                <p class="text-center"><strong>Current period</strong></p>
                <div id="pie-chart-current"></div>
              </div>
            </div>

            <div class="card shadow-0">
              <div class="card-body">
                <p class="text-center"><strong>Previous period</strong></p>
                <div id="pie-chart-previous"></div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!--Section: Content-->

    </div>
  </div>
</template>

<script>
  export default {

    mounted() {
      const sidenav = document.getElementById("main-sidenav");
      const sidenavInstance = mdb.Sidenav.getInstance(sidenav);

      let innerWidth = null;

      const setMode = (e) => {
        // Check necessary for Android devices
        if (window.innerWidth === innerWidth) {
          return;
        }

        innerWidth = window.innerWidth;

        if (window.innerWidth < 1400) {
          sidenavInstance.changeMode("over");
          sidenavInstance.hide();
        } else {
          sidenavInstance.changeMode("side");
          sidenavInstance.show();
        }
      };

      setMode();

      // Event listeners
      window.addEventListener("resize", setMode);

      const searchFocus = document.getElementById('search-focus');
      const keys = [{
          keyCode: 'AltLeft',
          isTriggered: false
        },
        {
          keyCode: 'ControlLeft',
          isTriggered: false
        },
      ];

      window.addEventListener('keydown', (e) => {
        keys.forEach((obj) => {
          if (obj.keyCode === e.code) {
            obj.isTriggered = true;
          }
        });

        const shortcutTriggered = keys.filter((obj) => obj.isTriggered).length === keys.length;

        if (shortcutTriggered) {
          searchFocus.focus();
        }
      });

      window.addEventListener('keyup', (e) => {
        keys.forEach((obj) => {
          if (obj.keyCode === e.code) {
            obj.isTriggered = false;
          }
        });
      });

      const dataLine = {
        type: "line",
        data: {
          labels: [
            "Monday",
            "Tuesday",
            "Wednesday",
            "Thursday",
            "Friday",
            "Saturday",
            "Sunday ",
          ],
          datasets: [{
              label: "Current period",
              data: [65, 59, 80, 81, 56, 55, 40],
            },
            {
              label: "Previous period",
              data: [28, 48, 40, 19, 86, 27, 90],
              backgroundColor: "rgba(66, 133, 244, 0.0)",
              borderColor: "#33b5e5",
              pointBorderColor: "#33b5e5",
              pointBackgroundColor: "#33b5e5",
            },
          ],
        },
      };

      new mdb.Chart(document.getElementById("chart-users"), dataLine);

      const dataPageViews = {
        type: "line",
        data: {
          labels: [
            "Monday",
            "Tuesday",
            "Wednesday",
            "Thursday",
            "Friday",
            "Saturday",
            "Sunday ",
          ],
          datasets: [{
              label: "Current period",
              data: [25, 49, 40, 21, 56, 75, 30],
            },
            {
              label: "Previous period",
              data: [58, 18, 30, 59, 46, 77, 90],
              backgroundColor: "rgba(66, 133, 244, 0.0)",
              borderColor: "#33b5e5",
              pointBorderColor: "#33b5e5",
              pointBackgroundColor: "#33b5e5",
            },
          ],
        },
      };

      new mdb.Chart(document.getElementById("chart-page-views"), dataPageViews);

      const dataAverageTime = {
        type: "line",
        data: {
          labels: [
            "Monday",
            "Tuesday",
            "Wednesday",
            "Thursday",
            "Friday",
            "Saturday",
            "Sunday ",
          ],
          datasets: [{
              label: "Current period",
              data: [431, 123, 435, 123, 345, 234, 124],
            },
            {
              label: "Previous period",
              data: [654, 234, 123, 432, 533, 422, 222],
              backgroundColor: "rgba(66, 133, 244, 0.0)",
              borderColor: "#33b5e5",
              pointBorderColor: "#33b5e5",
              pointBackgroundColor: "#33b5e5",
            },
          ],
        },
      };

      new mdb.Chart(
        document.getElementById("chart-average-time"),
        dataAverageTime
      );

      const dataBounceRate = {
        type: "line",
        data: {
          labels: [
            "Monday",
            "Tuesday",
            "Wednesday",
            "Thursday",
            "Friday",
            "Saturday",
            "Sunday ",
          ],
          datasets: [{
              label: "Current period",
              data: [41, 12, 35, 13, 45, 34, 12],
            },
            {
              label: "Previous period",
              data: [65, 24, 13, 43, 33, 42, 22],
              backgroundColor: "rgba(66, 133, 244, 0.0)",
              borderColor: "#33b5e5",
              pointBorderColor: "#33b5e5",
              pointBackgroundColor: "#33b5e5",
            },
          ],
        },
      };

      new mdb.Chart(document.getElementById("chart-bounce-rate"), dataBounceRate);

      const pieChartsOptions = {
        dataLabelsPlugin: true,
        options: {
          legend: {
            position: "right",
            labels: {
              boxWidth: 10,
            },
          },
          plugins: {
            datalabels: {
              formatter: (value, ctx) => {
                let sum = 0;
                let dataArr = dataPieCurrent.data.datasets[0].data;
                dataArr.map((data) => {
                  sum += data;
                });
                let percentage = ((value * 100) / sum).toFixed(2) + "%";
                return percentage;
              },
              color: "white",
              labels: {
                title: {
                  font: {
                    size: "14",
                  },
                },
              },
            },
          },
        },
      };

      // Pie chart current
      const dataPieCurrent = {
        type: "pie",
        data: {
          labels: ["New visitor", "Returning visitor"],
          datasets: [{
            label: "Logs",
            data: [502355, 423545],
            backgroundColor: [
              "rgba(66, 133, 244, 0.6)",
              "rgba(77, 182, 172, 0.6)",
            ],
          }, ],
        },
      };

      new mdb.Chart(
        document.getElementById("pie-chart-current"),
        dataPieCurrent,
        pieChartsOptions
      );

      // Pie chart previous
      const dataPiePrevious = {
        type: "pie",
        data: {
          labels: ["New visitor", "Returning visitor"],
          datasets: [{
            label: "Logs",
            data: [402355, 523545],
            backgroundColor: [
              "rgba(66, 133, 244, 0.6)",
              "rgba(77, 182, 172, 0.6)",
            ],
          }, ],
        },
      };

      new mdb.Chart(
        document.getElementById("pie-chart-previous"),
        dataPiePrevious,
        pieChartsOptions
      );
    },
    head: {
      title: 'Site Logs'
    }
  }

</script>
