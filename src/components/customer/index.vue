<template>
  <div>
    <div class="row">
      <router-link to="/store-employee" class="btn btn-primary ml-3">Add Customer</router-link>
    </div>
    <br>
    <input type="text"  @keyup="searchUnit" v-model="searchTerm" class="form-control" style="width: 300px;" placeholder="Search Here">
    <br>
    <div class="row">
      <div class="col-lg-12 mb-4">
        <!-- Simple Tables -->
        <div class="card">
          <div class="card-header py-3 d-flex flex-row align-items-center justify-content-between">
            <h6 class="m-0 font-weight-bold text-primary">Customer List</h6>
          </div>
          <div class="table-responsive">
            <table class="table align-items-center table-flush">
              <thead class="thead-light">
              <tr>
                <th>Name</th>
                <th>Email</th>
                <th>Phone</th>
                <th>Address</th>
                <th>Status</th>
                <th>Action</th>

              </tr>
              </thead>
              <tbody>
              <tr v-for="customer in customers.data" :key="customer.id">
                <td>{{ customer.name }}</td>
                <td>{{ customer.email }}</td>
                <td>{{ customer.phone }}</td>
                <td>{{ customer.address }}</td>
                <td>{{ customer.status.status_name}}</td>

                <td>
                  <router-link :to="{name: 'edit-customer', params:{id:customer.id}}" class="btn btn-sm btn-primary">Edit</router-link>&nbsp;
                  <a @click="deleteCustomer(customer.id)" class="btn btn-sm btn-danger"><font color="#ffffff">Delete</font></a>
                </td>
              </tr>

              </tbody>
            </table>
          </div>
          <div class="card-footer"></div>
        </div>

        <pagination :data="customers" @pagination-change-page="getResults" class="mt-4 float-right"></pagination>

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
      customers:{},
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
      this.$axios.get('http://127.0.0.1:8000/api/customer', {
        params: {
          page: page,
          q: (this.searchTerm == '' ? null : this.searchTerm)

        }
      }).then(response => {
        this.customers = response.data.data;

        //console.log(this.customers.data)
      })
    },

    searchUnit: debounce(function(){
      this.getResults()

    }),

    deleteCustomer(id){
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
          this.$axios.delete('http://127.0.0.1:8000/api/customer/'+ id)
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