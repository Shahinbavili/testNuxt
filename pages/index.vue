<template>

  <b-container>
<!--    <b-row>-->
<!--      <b-col>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci eaque illum iste pariatur, perspiciatis veniam?</b-col>-->
<!--      <b-col cols="8">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi beatae debitis delectus reiciendis vero voluptates.</b-col>-->
<!--      <b-col>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum omnis, quibusdam quis rerum temporibus voluptates?</b-col>-->
<!--    </b-row>-->
<!--    <p></p>-->
<!--      <div>-->
<!--        <button type="button" class="btn btn-primary">Primary</button>-->
<!--        <b-button>Button</b-button>-->
<!--        <b-button variant="danger">Button</b-button>-->
<!--        <b-button variant="success">Button</b-button>-->
<!--        <b-button variant="outline-primary">Button</b-button>-->
<!--        <b-button variant="dark">Dark</b-button>-->
<!--        <hr>-->
<!--        <button type="button" class="btn btn-primary">Primary</button>-->
<!--        <button type="button" class="btn btn-secondary">Secondary</button>-->
<!--        <button type="button" class="btn btn-success">Success</button>-->
<!--        <button type="button" class="btn btn-danger">Danger</button>-->
<!--        <button type="button" class="btn btn-warning">Warning</button>-->
<!--        <button type="button" class="btn btn-info">Info</button>-->
<!--        <button type="button" class="btn btn-light">Light</button>-->
<!--        <b-button variant="dark">Dark</b-button>-->


<!--        <button type="button" class="btn btn-link">Link</button>-->
<!--      </div>-->
<!--    <div>-->
<!--      <b-dropdown id="dropdown-1" text="Dropdown Button" class="m-md-2">-->
<!--        <b-dropdown-item>First Action</b-dropdown-item>-->
<!--        <b-dropdown-item>Second Action</b-dropdown-item>-->
<!--        <b-dropdown-item>Third Action</b-dropdown-item>-->
<!--        <b-dropdown-divider></b-dropdown-divider>-->
<!--        <b-dropdown-item active>Active action</b-dropdown-item>-->
<!--        <b-dropdown-item disabled>Disabled action</b-dropdown-item>-->
<!--      </b-dropdown>-->
<!--    </div>-->
<!--    <div>-->
<!--      <b-form @submit="onSubmit" @reset="onReset" v-if="show">-->
<!--        <b-form-group-->
<!--          id="input-group-1"-->
<!--          label="Email address:"-->
<!--          label-for="input-1"-->
<!--          description="We'll never share your email with anyone else."-->
<!--        >-->
<!--          <b-form-input-->
<!--            id="input-1"-->
<!--            v-model="form.email"-->
<!--            type="email"-->
<!--            placeholder="Enter email"-->
<!--            required-->
<!--          ></b-form-input>-->
<!--        </b-form-group>-->

<!--        <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">-->
<!--          <b-form-input-->
<!--            id="input-2"-->
<!--            v-model="form.name"-->
<!--            placeholder="Enter name"-->
<!--            required-->
<!--          ></b-form-input>-->
<!--        </b-form-group>-->

<!--        <b-form-group id="input-group-3" label="Food:" label-for="input-3">-->
<!--          <b-form-select-->
<!--            id="input-3"-->
<!--            v-model="form.food"-->
<!--            :options="foods"-->
<!--            required-->
<!--          ></b-form-select>-->
<!--        </b-form-group>-->

<!--        <b-form-group id="input-group-4" v-slot="{ ariaDescribedby }">-->
<!--          <b-form-checkbox-group-->
<!--            v-model="form.checked"-->
<!--            id="checkboxes-4"-->
<!--            :aria-describedby="ariaDescribedby"-->
<!--          >-->
<!--            <b-form-checkbox value="me">Check me out</b-form-checkbox>-->
<!--            <b-form-checkbox value="that">Check that out</b-form-checkbox>-->
<!--          </b-form-checkbox-group>-->
<!--        </b-form-group>-->

<!--        <b-button type="submit" variant="primary">Submit</b-button>-->
<!--        <b-button type="reset" variant="danger">Reset</b-button>-->
<!--      </b-form>-->
<!--      <b-card class="mt-3" header="Form Data Result">-->
<!--        <pre class="m-0">{{ form }}</pre>-->
<!--      </b-card>-->
<!--    </div>-->
    <hr>
    <div>
      <nuxt-link to="/products">products</nuxt-link>

    </div>
  </b-container>

</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
      show: true
    }
  },
  methods: {
    onSubmit(event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset(event) {
      event.preventDefault()
      // Reset our form values
      this.form.email = ''
      this.form.name = ''
      this.form.food = null
      this.form.checked = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>


