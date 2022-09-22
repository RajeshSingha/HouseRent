<template>
  <v-container fluid>

<!--    <v-form v-model="valid">
      <v-row align="center">
        <v-col cols="3">
          <v-row>
            <h1 class="display-1 text-left mb-5">Personal Information</h1>
          </v-row>
          <v-row>
            <v-text-field v-model="firstname" :rules="nameRules" :counter="10" label="First name" required
            ></v-text-field>
          </v-row>

          <v-row>
            <v-text-field v-model="lastname" :rules="nameRules" :counter="10" label="Last name" required></v-text-field>
          </v-row>

          <v-row>
            <v-text-field v-model="email" :rules="emailRules" label="E-mail" required
            ></v-text-field>
          </v-row>
        </v-col>

        <v-col cols="3" class="ml-16">
          <v-row>
            <h1 class="display-1 mb-4">House Information</h1>
          </v-row>
          <v-row>
            <v-text-field v-model="bedroomCount" :rules="nameRules" label="Bedroom Count"
            ></v-text-field>
          </v-row>
          <v-row>
            <v-text-field v-model="kitchenCount" :rules="nameRules" label="Kitchen Count"
            ></v-text-field>
          </v-row>
          <v-row>
            <v-text-field v-model="washroomCount" :rules="nameRules" label="Washroom Count" ></v-text-field>
          </v-row>
          <v-row>
            <v-text-field v-model="floorNumber" :rules="emailRules" label="Floor Number"
            ></v-text-field>
          </v-row>
          <v-row cols="4" md="4" class="pa-0">
            <v-col wrap cols="4" class="pa-0 text-left">
              <span class="text-sm-h6 pa-0">Has Elevator</span>
            </v-col>
            <v-col cols="2" class="pa-0 text-start">
              <v-checkbox @click="hasElevatorClicked"></v-checkbox>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-form>-->

    <v-row justify="center">
      <v-col md="4" class="pa-6">

        <v-row class="mb-8">
          <h1 class="text-sm-h4 font-weight-bold">Personal Information</h1>
        </v-row>
        <v-row class="mb-1" >
          <v-text-field label="First Name"></v-text-field>
        </v-row>
        <v-row class="mb-1">
          <v-text-field label="Middle Name"></v-text-field>
        </v-row>
        <v-row class="mb-1">
         <v-text-field label="Last Name"></v-text-field>
        </v-row>
        <v-row class="mb-1">
          <v-text-field label="Gmail"></v-text-field>
        </v-row>
        <v-row class="mb-1">
          <v-btn class="pink">Submit</v-btn>
        </v-row>
      </v-col>

      <v-col md="4" class="pa-6">
        <v-row class="mb-8">
          <h1 class="text-sm-h4 font-weight-bold">House Information</h1>
        </v-row>
        <v-row class="mb-1">
          <v-text-field label="Number of Room"></v-text-field>
        </v-row>
        <v-row class="mb-1">
          <v-text-field label="Number of Kitchen"></v-text-field>
        </v-row>
        <v-row class="mb-1">
          <v-text-field label="Number of Washroom"></v-text-field>
        </v-row>
        <v-row class="mb-1">
          <v-checkbox>hello</v-checkbox>
        </v-row>
      </v-col>


    </v-row>


  </v-container>
</template>

<script>
export default {
  data: () => {
    return {
      valid: false,
      firstname: '',
      lastname: '',
      bedroomCount: 0,
      kitchenCount: 0,
      washroomCount: 0,
      floorNumber: 0,
      hasElevator: false,

      nameRules: [
        v => {
          return !!v || 'Name is required';
        },
        v => v.length <= 10 || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
    };
  },
  methods: {
    hasElevatorClicked: function (){
      this.hasElevator = true;
    }
  },
}
</script>