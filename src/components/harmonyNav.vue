<template>
  <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav  class="ml-auto">
        <b-nav-form>
          <b-nav-item class="px-3" href="#">Home Page</b-nav-item>
          <b-nav-item class="px-3" href="#">Manual Edit</b-nav-item>
          <b-nav-item class="px-3" href="#">Employees</b-nav-item>
          <b-nav-item class="px-3" href="#">Work Schedule</b-nav-item>
          <b-nav-item class="px-3" href="#">Reports</b-nav-item>
          <b-nav-item class="px-3" href="#">Maintenance</b-nav-item>
          <b-nav-item class="px-3" href="#">Documents</b-nav-item>
          <b-form-input dir="rtl" size="sm" list="my-list-id" class="mr-sm-2" placeholder="Select Country"></b-form-input>
          <datalist id="my-list-id">
              <option v-for="(country,index) in countries" :key="index">{{ country }}</option>
          </datalist>
        </b-nav-form>
      </b-navbar-nav>
    </b-collapse>
    
  </b-navbar>
</template>

<script>
import countries from "@/utils/country_list"
export default {
  data(){
        return {
            countries: countries
        }
    }
}
</script>

<style>

</style>