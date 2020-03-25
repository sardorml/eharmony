<template>
  <div class="container">
      <div class="row">
          <div class="col-xl-12 d-flex align-items-end flex-column">
              <h4 class="text-primary">Lorem</h4>
          </div>
          <div class="col-xl-12 d-flex align-items-end flex-column">
              <b-form-group>
                <b-form-radio-group buttons
                    button-variant="outline-primary"
                    size="sm"
                    name="radio-btn-outline">
                    <b-form-radio v-model="selected" name="some-radios" value="A">Option A</b-form-radio>
                    <b-form-radio v-model="selected" name="some-radios" value="B">Option B</b-form-radio>
                    <h4 class="ml-5">lorem*</h4>
                </b-form-radio-group>
            </b-form-group>
          </div>
          <div class="col-xl-12 d-flex align-items-end flex-column">
              <div>
                  <b-form-datepicker id="example-datepicker" class="mb-2"></b-form-datepicker>
                <b-input-group class="mb-3">
                    <b-input-group-append>
                        <b-form-datepicker
                        v-model="value"
                        button-only
                        right
                        locale="en-US"
                        aria-controls="example-input"
                        ></b-form-datepicker>
                    </b-input-group-append>
                    <b-form-input
                        id="example-input"
                        v-model="value"
                        type="text"
                        placeholder="YYYY-MM-DD"
                        dir="rtl"
                    ></b-form-input>
                </b-input-group>
              </div>
          </div>
          <div class="col-xl-12 d-flex align-items-end flex-column">
              <div>
                  <b-form-select
                    v-model="selected"
                    :options="options"
                    class="mb-3"
                    value-field="item"
                    text-field="name"
                    disabled-field="notEnabled"
                ></b-form-select>

                <div><strong>{{ selected }}</strong> :Selected</div>
              </div>
          </div>
            <div class="col-xl-12 d-flex align-items-end flex-column">
               <div class="mt-2">
                    <b-form-input dir="rtl" list="my-list-id" placeholder="Select Country"></b-form-input>

                    <datalist id="my-list-id">
                        <option v-for="(country,index) in countries" :key="index">{{ country }}</option>
                    </datalist>
               </div>
            </div>
            <div class="col-xl-12 d-flex align-items-end flex-column">
                <div>
                     <b-input-group class="mt-2">
                        <b-input-group-prepend is-text>
                        <input type="checkbox" aria-label="Checkbox for following text input">
                        </b-input-group-prepend>
                        <b-form-input dir="rtl" aria-label="Text input with checkbox"></b-form-input>
                    </b-input-group>
                </div>     
            </div>
      </div>
  </div>
</template>

<script>
import countries from "@/utils/country_list"
export default {
    data(){
        return {
            value: '',
            selected: 'A',
            options: [
                { item: 'A', name: 'Option A' },
                { item: 'B', name: 'Option B' },
                { item: 'D', name: 'Option C', notEnabled: true },
                { item: { d: 1 }, name: 'Option D' }
            ],
            countries: countries
        }
    }
}
</script>

<style>

</style>