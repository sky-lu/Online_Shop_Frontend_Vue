<template>
  <div>
    <div class="row">
      <router-link to="/store-employee" class="btn btn-primary ml-3">Add Employee</router-link>
    </div>
    <br>
    <input type="text"  @keyup="searchUnit" v-model="searchTerm" class="form-control" style="width: 300px;" placeholder="Search Here">
    <br>
    <div class="row">
      <div class="col-lg-12 mb-4">
        <!-- Simple Tables -->
        <div class="card">
          <div class="card-header py-3 d-flex flex-row align-items-center justify-content-between">
            <h6 class="m-0 font-weight-bold text-primary">Employee List</h6>
          </div>
          <div class="table-responsive">
            <table class="table align-items-center table-flush">
              <thead class="thead-light">
              <tr>
                <th>Name</th>
                <th>Email</th>
                <th>Phone</th>
                <th>Address</th>
                <th>Birth Date</th>
                <th>Department</th>
                <th class="text-center">Contract</th>
                <th class="text-center">Action</th>

              </tr>
              </thead>
              <tbody>
              <tr v-for="employee in employees.data" :key="employee.id">
                <td>{{ employee.name }}</td>
                <td>{{ employee.email }}</td>
                <td>{{ employee.phone }}</td>
                <td>{{ employee.address }}</td>
                <td>{{ employee.birthdate }}</td>
                <td>{{ employee.department.name }}</td>
                <td class="text-center">
                  <router-link v-if="employee.contract_id == null" :to="{name: 'store-contract', params:{id:employee.id}}" class="btn btn-sm btn-warning"><font-awesome-icon :icon="['fas', 'plus-square']" size="1x"/></router-link>
                  <router-link v-else :to="{name: 'view-contract', params:{id:employee.id}}" class="btn btn-sm btn-info"><font-awesome-icon :icon="['fas', 'file-contract']" size="1x"/></router-link>
                </td>

                <td>
                  <router-link :to="{name: 'edit-employee', params:{id:employee.id}}" class="btn btn-sm btn-primary">Edit</router-link>&nbsp;
                  <a @click="deleteEmployee(employee.id)" class="btn btn-sm btn-danger"><font color="#ffffff">Delete</font></a>
                </td>
              </tr>

              </tbody>
            </table>
          </div>
          <div class="card-footer"></div>
        </div>

        <pagination :data="employees" @pagination-change-page="getResults" class="mt-4 float-right"></pagination>

      </div>
    </div>

    <!--Row-->
  </div>
</template>

<script>
  import pagination from "laravel-vue-pagination";
  import {debounce} from "lodash";

  export default {
    components : { pagination },
    // created() {
    //
    // },
    data(){
      return{
        employees:{},
        searchTerm: null,
        page: 1
      }
    },

    mounted() {
      // Fetch initial results
      this.getResults();
    },




    methods:{


      getResults(page = 1) {
        this.page = page
        this.$axios.get('http://127.0.0.1:8000/api/employee', {
          params: {
            page: page,
            q: (this.searchTerm == '' ? null : this.searchTerm)

          }
        }).then(response => {
              this.employees= response.data.data;

              console.log(this.employees.data)
            })
      },

      searchUnit: debounce(function(){
        this.getResults()

      }),

      deleteEmployee(id){
        this.$swal.fire({
          title: 'Are you sure?',
          text: "You won't be able to revert this!",
          icon: 'warning',
          showCancelButton: true,
          confirmButtonColor: '#3085d6',
          cancelButtonColor: '#d33',
          confirmButtonText: 'Yes, delete it!'
        }).then((result) => {
          if (result.isConfirmed) {
            this.$axios.delete('http://127.0.0.1:8000/api/employee/'+ id)
                .then(() => {
                  this.getResults(this.page)

                })
                .catch(() => {
                  // this.$router.push({name: 'employee'})
                })

                this.$swal.fire(
                'Deleted!',
                'Your file has been deleted.',
                'success'
              )
          }
        })

      },
    }


  }

</script>

<style>

</style>