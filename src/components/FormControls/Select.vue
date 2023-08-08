<template>
    <h2 class="text-center">Select</h2>
    <v-row>
        <v-col cols="3">
            <v-select
            v-model="favorites"
            hint="pick your fav states"
            :items="states"
            persistent-hint
            label="select"
            multiple
            color="red"
            ></v-select>
        </v-col>
        <v-col cols="3">
            <v-select
            :items="items"
            item-title="state"
            item-value="abbr"
            label="select state"
            :hint="`${select.state}, ${select.abbr}`"
            persistent-hint
            v-model="select"
            return-object
            single-line
            ></v-select>
        </v-col>
    </v-row>
    
</template>
<script>
  export default {
    data () {
      return {
        favorites: [],
        states: [
          'Alabama', 'Alaska', 'American Samoa', 'Arizona',
          'Arkansas', 'California', 'Colorado', 'Connecticut',
          'Delaware', 'District of Columbia', 'Federated States of Micronesia',
          'Florida', 'Georgia', 'Guam', 'Hawaii', 'Idaho',
          'Illinois', 'Indiana', 'Iowa', 'Kansas', 'Kentucky',
          'Louisiana', 'Maine', 'Marshall Islands', 'Maryland',
          'Massachusetts', 'Michigan', 'Minnesota', 'Mississippi',
          'Missouri', 'Montana', 'Nebraska', 'Nevada',
          'New Hampshire', 'New Jersey', 'New Mexico', 'New York',
          'North Carolina', 'North Dakota', 'Northern Mariana Islands', 'Ohio',
          'Oklahoma', 'Oregon', 'Palau', 'Pennsylvania', 'Puerto Rico',
          'Rhode Island', 'South Carolina', 'South Dakota', 'Tennessee',
          'Texas', 'Utah', 'Vermont', 'Virgin Island', 'Virginia',
          'Washington', 'West Virginia', 'Wisconsin', 'Wyoming',
        ],
        select: { state: 'Florida', abbr: 'FL' },
        items: [
          { state: 'Florida', abbr: 'FL' },
          { state: 'Georgia', abbr: 'GA' },
          { state: 'Nebraska', abbr: 'NE' },
          { state: 'California', abbr: 'CA' },
          { state: 'New York', abbr: 'NY' },
        ],
      }
    },
  }
</script>