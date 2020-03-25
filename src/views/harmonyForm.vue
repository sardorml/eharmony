<template>
  <div>
    <b-tabs content-class="mt-3" active-nav-item-class="text-uppercase bg-warning text-primary">
        <b-tab title="Display pay checks" disabled><p>I'm the first tab</p></b-tab>
        <b-tab title="Form 101" active>
          <div class="container-fluid">
            <div class="row">
              <div class="col-xl-2 col-12">
                <b-button-group class="mt-2">
                  <b-button @click="tabIndex--">Previous</b-button>
                  <b-button @click="tabIndex++">Next</b-button>
                </b-button-group>
              </div>
              <div class="text-right col-5 offset-xl-4 col-xl-2">
                <p>2019 <span class="text-success font-weight-bold" >:Tax Year</span> </p>
              </div>
              <div class="text-right col-xl-2 col-3">
                <p>lorem :Status</p>
              </div>
              <div class="text-right col-xl-2 col-4">
                <p>1 :Version</p>
              </div>
            </div>
          </div>
          <b-card no-body class="border-0">
            <b-tabs active-nav-item-class="bg-info" class="d-flex justify-content-center" pills fill card vertical end v-model="tabIndex">
              <b-tab title="Employer details"><b-card-text>Tab contents 1</b-card-text></b-tab>
              <b-tab title="Employee details">
                <harmony-content></harmony-content>
              </b-tab>
              <b-tab title="Bank Account Details"><b-card-text>Tab contents 3</b-card-text></b-tab>
              <b-tab title="Children details (minors)"><b-card-text>Tab contents</b-card-text></b-tab>
              <b-tab title="Income from current employer"><b-card-text>Tab contents</b-card-text></b-tab>
              <b-tab title="Other incomes"><b-card-text>Tab contents</b-card-text></b-tab>
              <b-tab title="Spouse details" disabled><b-card-text>Tab contents</b-card-text></b-tab>
              <b-tab title="Income tax exemtion request"><b-card-text>Tab contents</b-card-text></b-tab>
              <b-tab title="Tax coordination request"><b-card-text>Tab contents</b-card-text></b-tab>
              <b-tab title="Statement"><b-card-text>Tab contents</b-card-text></b-tab>
            </b-tabs>
          </b-card>
        </b-tab>
        <b-tab title="Display Form 106" disabled><p>I'm a disabled tab!</p></b-tab>
        <b-tab title="Employee Documents" disabled><p>I'm a disabled tab!</p></b-tab>
        <b-tab title="Digital Documents" disabled><p>I'm a disabled tab!</p></b-tab>
    </b-tabs>
    </div>
</template>

<script>
import harmonyContent from '../components/content'
export default {
  components:{
    harmonyContent
  },
  data(){
    return {
      tabIndex: 1
    }
  }
}
</script>

<style>

</style>