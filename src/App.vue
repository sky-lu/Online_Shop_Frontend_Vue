<template>
  <div id="app">
    <div id="wrapper">
      <!-- Sidebar -->
      <ul class="navbar-nav sidebar sidebar-light accordion" id="accordionSidebar">
        <a class="sidebar-brand d-flex align-items-center justify-content-center" href="index.html">
          <div class="sidebar-brand-icon">
            <img src="backend/img/logo/logo2.png">
          </div>
          <div class="sidebar-brand-text mx-3">RuangAdmin</div>
        </a>
        <hr class="sidebar-divider my-0">
        <li class="nav-item active">
          <a class="nav-link" href="index.html">
            <i class="fas fa-fw fa-tachometer-alt"></i>
            <span>Dashboard</span></a>
        </li>
        <hr class="sidebar-divider">
        <div class="sidebar-heading">
          Features
        </div>
        <!--employees Part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap"
             aria-expanded="true" aria-controls="collapseBootstrap">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Employees</span>
          </a>
          <div id="collapseBootstrap" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-employee">Add Employee</router-link>
              <router-link class="collapse-item" to="/employee">All Employees</router-link>
            </div>
          </div>
        </li>
        <!--contracts Part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap2"
             aria-expanded="true" aria-controls="collapseBootstrap2">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Contracts</span>
          </a>
          <div id="collapseBootstrap2" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-contract">Add Contract</router-link>
              <router-link class="collapse-item" to="/contract">All Contracts</router-link>
            </div>
          </div>
        </li>
        <!--customers Part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap3"
             aria-expanded="true" aria-controls="collapseBootstrap3">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Customers</span>
          </a>
          <div id="collapseBootstrap3" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-customer">Add Customer</router-link>
              <router-link class="collapse-item" to="/customer">All Customers</router-link>
            </div>
          </div>
        </li>
        <!--suppliers Part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap1"
             aria-expanded="true" aria-controls="collapseBootstrap1">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Suppliers</span>
          </a>
          <div id="collapseBootstrap1" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-supplier">Add Supplier</router-link>
              <router-link class="collapse-item" to="/supplier">All Suppliers</router-link>
            </div>
          </div>
        </li>
        <!--products part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap4"
             aria-expanded="true" aria-controls="collapseBootstrap4">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Products</span>
          </a>
          <div id="collapseBootstrap4" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-product">Add Product</router-link>
              <router-link class="collapse-item" to="/product">All Products</router-link>
            </div>
          </div>
        </li>
        <!--feedback part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap5"
             aria-expanded="true" aria-controls="collapseBootstrap5">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Feedback</span>
          </a>
          <div id="collapseBootstrap5" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
<!--              <router-link class="collapse-item" to="/store-product">Add Product</router-link>-->
              <router-link class="collapse-item" to="/feedback">All Feedback</router-link>
            </div>
          </div>
        </li>
        <!--vat part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap6"
             aria-expanded="true" aria-controls="collapseBootstrap6">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Vats</span>
          </a>
          <div id="collapseBootstrap6" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-vat">Add Vat</router-link>
              <router-link class="collapse-item" to="/vat">All Vats</router-link>
            </div>
          </div>
        </li>
        <!--article category part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap7"
             aria-expanded="true" aria-controls="collapseBootstrap7">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Article Categories</span>
          </a>
          <div id="collapseBootstrap7" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/article-category">All Article Categories</router-link>
            </div>
          </div>
        </li>
        <!--article part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap8"
             aria-expanded="true" aria-controls="collapseBootstrap8">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Articles</span>
          </a>
          <div id="collapseBootstrap8" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/store-article">Add Article</router-link>
              <router-link class="collapse-item" to="/article">All Articles</router-link>
            </div>
          </div>
        </li>
        <!--order part-->
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseBootstrap9"
             aria-expanded="true" aria-controls="collapseBootstrap9">
            <i class="far fa-fw fa-window-maximize"></i>
            <span>Orders</span>
          </a>
          <div id="collapseBootstrap9" class="collapse" aria-labelledby="headingBootstrap" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <router-link class="collapse-item" to="/order">All Orders</router-link>
            </div>
          </div>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="forms.html">
            <i class="fab fa-fw fa-wpforms"></i>
            <span>Forms</span>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapseTable" aria-expanded="true"
             aria-controls="collapseTable">
            <i class="fas fa-fw fa-table"></i>
            <span>Tables</span>
          </a>
          <div id="collapseTable" class="collapse" aria-labelledby="headingTable" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <h6 class="collapse-header">Tables</h6>
              <a class="collapse-item" href="simple-tables.html">Simple Tables</a>
              <a class="collapse-item" href="datatables.html">DataTables</a>
            </div>
          </div>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="ui-colors.html">
            <i class="fas fa-fw fa-palette"></i>
            <span>UI Colors</span>
          </a>
        </li>
        <hr class="sidebar-divider">
        <div class="sidebar-heading">
          Examples
        </div>
        <li class="nav-item">
          <a class="nav-link collapsed" href="#" data-toggle="collapse" data-target="#collapsePage" aria-expanded="true"
             aria-controls="collapsePage">
            <i class="fas fa-fw fa-columns"></i>
            <span>Pages</span>
          </a>
          <div id="collapsePage" class="collapse" aria-labelledby="headingPage" data-parent="#accordionSidebar">
            <div class="bg-white py-2 collapse-inner rounded">
              <h6 class="collapse-header">Example Pages</h6>
              <a class="collapse-item" href="login.html">Login</a>
              <a class="collapse-item" href="register.html">Register</a>
              <a class="collapse-item" href="404.html">404 Page</a>
              <a class="collapse-item" href="blank.html">Blank Page</a>
            </div>
          </div>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="charts.html">
            <i class="fas fa-fw fa-chart-area"></i>
            <span>Charts</span>
          </a>
        </li>
        <hr class="sidebar-divider">
        <div class="version" id="version-ruangadmin"></div>
      </ul>
      <!-- Sidebar -->
      <div id="content-wrapper" class="d-flex flex-column">
        <div id="content">
          <!-- TopBar -->
          <nav class="navbar navbar-expand navbar-light bg-navbar topbar mb-4 static-top">
            <button id="sidebarToggleTop" class="btn btn-link rounded-circle mr-3">
              <i class="fa fa-bars"></i>
            </button>
            <ul class="navbar-nav ml-auto">
              <li class="nav-item dropdown no-arrow">
                <a class="nav-link dropdown-toggle" href="#" id="searchDropdown" role="button" data-toggle="dropdown"
                   aria-haspopup="true" aria-expanded="false">
                  <i class="fas fa-search fa-fw"></i>
                </a>
                <div class="dropdown-menu dropdown-menu-right p-3 shadow animated--grow-in"
                     aria-labelledby="searchDropdown">
                  <form class="navbar-search">
                    <div class="input-group">
                      <input type="text" class="form-control bg-light border-1 small" placeholder="What do you want to look for?"
                             aria-label="Search" aria-describedby="basic-addon2" style="border-color: #3f51b5;">
                      <div class="input-group-append">
                        <button class="btn btn-primary" type="button">
                          <i class="fas fa-search fa-sm"></i>
                        </button>
                      </div>
                    </div>
                  </form>
                </div>
              </li>
              <li class="nav-item dropdown no-arrow mx-1">
                <a class="nav-link dropdown-toggle" href="#" id="alertsDropdown" role="button" data-toggle="dropdown"
                   aria-haspopup="true" aria-expanded="false">
                  <i class="fas fa-bell fa-fw"></i>
                  <span class="badge badge-danger badge-counter">3+</span>
                </a>
                <div class="dropdown-list dropdown-menu dropdown-menu-right shadow animated--grow-in"
                     aria-labelledby="alertsDropdown">
                  <h6 class="dropdown-header">
                    Alerts Center
                  </h6>
                  <a class="dropdown-item d-flex align-items-center" href="#">
                    <div class="mr-3">
                      <div class="icon-circle bg-primary">
                        <i class="fas fa-file-alt text-white"></i>
                      </div>
                    </div>
                    <div>
                      <div class="small text-gray-500">December 12, 2019</div>
                      <span class="font-weight-bold">A new monthly report is ready to download!</span>
                    </div>
                  </a>
                  <a class="dropdown-item d-flex align-items-center" href="#">
                    <div class="mr-3">
                      <div class="icon-circle bg-success">
                        <i class="fas fa-donate text-white"></i>
                      </div>
                    </div>
                    <div>
                      <div class="small text-gray-500">December 7, 2019</div>
                      $290.29 has been deposited into your account!
                    </div>
                  </a>
                  <a class="dropdown-item d-flex align-items-center" href="#">
                    <div class="mr-3">
                      <div class="icon-circle bg-warning">
                        <i class="fas fa-exclamation-triangle text-white"></i>
                      </div>
                    </div>
                    <div>
                      <div class="small text-gray-500">December 2, 2019</div>
                      Spending Alert: We've noticed unusually high spending for your account.
                    </div>
                  </a>
                  <a class="dropdown-item text-center small text-gray-500" href="#">Show All Alerts</a>
                </div>
              </li>
              <li class="nav-item dropdown no-arrow mx-1">
                <a class="nav-link dropdown-toggle" href="#" id="messagesDropdown" role="button" data-toggle="dropdown"
                   aria-haspopup="true" aria-expanded="false">
                  <i class="fas fa-envelope fa-fw"></i>
                  <span class="badge badge-warning badge-counter">2</span>
                </a>
                <div class="dropdown-list dropdown-menu dropdown-menu-right shadow animated--grow-in"
                     aria-labelledby="messagesDropdown">
                  <h6 class="dropdown-header">
                    Message Center
                  </h6>
                  <a class="dropdown-item d-flex align-items-center" href="#">
                    <div class="dropdown-list-image mr-3">
                      <img class="rounded-circle" src="backend/img/man.png" style="max-width: 60px" alt="">
                      <div class="status-indicator bg-success"></div>
                    </div>
                    <div class="font-weight-bold">
                      <div class="text-truncate">Hi there! I am wondering if you can help me with a problem I've been
                        having.</div>
                      <div class="small text-gray-500">Udin Cilok · 58m</div>
                    </div>
                  </a>
                  <a class="dropdown-item d-flex align-items-center" href="#">
                    <div class="dropdown-list-image mr-3">
                      <img class="rounded-circle" src="backend/img/girl.png" style="max-width: 60px" alt="">
                      <div class="status-indicator bg-default"></div>
                    </div>
                    <div>
                      <div class="text-truncate">Am I a good boy? The reason I ask is because someone told me that people
                        say this to all dogs, even if they aren't good...</div>
                      <div class="small text-gray-500">Jaenab · 2w</div>
                    </div>
                  </a>
                  <a class="dropdown-item text-center small text-gray-500" href="#">Read More Messages</a>
                </div>
              </li>
              <li class="nav-item dropdown no-arrow mx-1">
                <a class="nav-link dropdown-toggle" href="#" id="messagesDropdown1" role="button" data-toggle="dropdown"
                   aria-haspopup="true" aria-expanded="false">
                  <i class="fas fa-tasks fa-fw"></i>
                  <span class="badge badge-success badge-counter">3</span>
                </a>
                <div class="dropdown-list dropdown-menu dropdown-menu-right shadow animated--grow-in"
                     aria-labelledby="messagesDropdown">
                  <h6 class="dropdown-header">
                    Task
                  </h6>
                  <a class="dropdown-item align-items-center" href="#">
                    <div class="mb-3">
                      <div class="small text-gray-500">Design Button
                        <div class="small float-right"><b>50%</b></div>
                      </div>
                      <div class="progress" style="height: 12px;">
                        <div class="progress-bar bg-success" role="progressbar" style="width: 50%" aria-valuenow="50"
                             aria-valuemin="0" aria-valuemax="100"></div>
                      </div>
                    </div>
                  </a>
                  <a class="dropdown-item align-items-center" href="#">
                    <div class="mb-3">
                      <div class="small text-gray-500">Make Beautiful Transitions
                        <div class="small float-right"><b>30%</b></div>
                      </div>
                      <div class="progress" style="height: 12px;">
                        <div class="progress-bar bg-warning" role="progressbar" style="width: 30%" aria-valuenow="30"
                             aria-valuemin="0" aria-valuemax="100"></div>
                      </div>
                    </div>
                  </a>
                  <a class="dropdown-item align-items-center" href="#">
                    <div class="mb-3">
                      <div class="small text-gray-500">Create Pie Chart
                        <div class="small float-right"><b>75%</b></div>
                      </div>
                      <div class="progress" style="height: 12px;">
                        <div class="progress-bar bg-danger" role="progressbar" style="width: 75%" aria-valuenow="75"
                             aria-valuemin="0" aria-valuemax="100"></div>
                      </div>
                    </div>
                  </a>
                  <a class="dropdown-item text-center small text-gray-500" href="#">View All Taks</a>
                </div>
              </li>
              <div class="topbar-divider d-none d-sm-block"></div>
              <li class="nav-item dropdown no-arrow">
                <a class="nav-link dropdown-toggle" href="#" id="userDropdown" role="button" data-toggle="dropdown"
                   aria-haspopup="true" aria-expanded="false">
                  <img class="img-profile rounded-circle" src="backend/img/boy.png" style="max-width: 60px">
                  <span class="ml-2 d-none d-lg-inline text-white small">Maman Ketoprak</span>
                </a>
                <div class="dropdown-menu dropdown-menu-right shadow animated--grow-in" aria-labelledby="userDropdown">
                  <a class="dropdown-item" href="#">
                    <i class="fas fa-user fa-sm fa-fw mr-2 text-gray-400"></i>
                    Profile
                  </a>
                  <a class="dropdown-item" href="#">
                    <i class="fas fa-cogs fa-sm fa-fw mr-2 text-gray-400"></i>
                    Settings
                  </a>
                  <a class="dropdown-item" href="#">
                    <i class="fas fa-list fa-sm fa-fw mr-2 text-gray-400"></i>
                    Activity Log
                  </a>
                  <div class="dropdown-divider"></div>
                  <a class="dropdown-item" href="login.html">
                    <i class="fas fa-sign-out-alt fa-sm fa-fw mr-2 text-gray-400"></i>
                    Logout
                  </a>
                </div>
              </li>
            </ul>
          </nav>
          <!-- Topbar -->

          <!-- Container Fluid-->
          <div class="container-fluid" id="container-wrapper">
              <router-view />
          </div>
          <!---Container Fluid-->
        </div>

      </div>
    </div>
  </div>
</template>

<script>

//import Login from './components/auth/login.vue'

export default {
  name: 'App',
  data() {
    return {
      // configuration: {"contract":{"type":{"permanent":0,"fixed-term":1,"casual":2}},"customer":{"status":{"normal":0,"unormal":1}},"supplier":{"status":{"normal":0,"unormal":1}},"product":{"status":{"on-sale":0,"off-shelf":1}}}
      configuration: null
    }

  },
  mounted() {

  },
  async created() {
    try {
      let res = await this.getConfiguration()
      this.configuration = res.data.data
    } catch (e) {
      console.log(e)
    }

  },
  methods: {
    // try {
    //   let res = await this.$axios.get('http://127.0.0.1:8000/api/configure')
    //   // console.log(res.data.data)
    //   this.configuration = res.data.data
    // } catch (e) {
    //   console.log(e)
    // }
    getConfiguration() {
      return new Promise((resolve, reject) => {
        this.$axios.get('http://127.0.0.1:8000/api/configure').then((res) => {
          resolve(res)
        }).catch((err) => {
          reject(err)
        })
      })
    }
  }


}
</script>

<style>

</style>
