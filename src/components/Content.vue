<template>
<div>
  <table>
    <tr>
      <th>Person last name</th>
      <th>Person first name</th>
      <th>Person age</th>
      <th>Address.city</th>
      <th>Country</th>
    </tr>
    <tr v-for="(item,index) in items" :key="index" :class="{ 'danger': item.isDanger}">
      <td>{{item.last_name}}</td>
      <td>{{item.first_name}}</td>
      <td>{{item.age}}</td>
      <td>{{item.address.city}}</td>
      <td>{{item.address.country}}</td>
    </tr>
  </table>
  <Card></Card>
</div>
</template>

<script>
import Card from "@/components/Card.vue";
export default {
  components: {
    Card
  },
  data() {
    return {
      // Note 'isActive' is left out and will not appear in the rendered table
      fields: {
        last_name: {
          label: 'Person last name',
          sortable: true
        },
        first_name: {
          label: 'Person first name',
          sortable: false
        },
        foo: {
          // This key overrides `foo`!
          key: 'age',
          label: 'Person age',
          sortable: true
        },
        city: {
          key: 'address.city',
          sortable: true
        },
        'address.country': {
          label: 'Country',
          sortable: true
        }
      },
      items: [{
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
            isActive: true,
            age: 40,
            first_name: 'Dickerson',
            last_name: 'Macdonald',
            address: {
              country: 'USA',
              city: 'New York'
            },
            isDanger: true
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: true
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: true
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: true
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: true
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: true
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: true,
          age: 40,
          first_name: 'Dickerson',
          last_name: 'Macdonald',
          address: {
            country: 'USA',
            city: 'New York'
          },
          isDanger: true
        },
        {
          isActive: true,
          age: 38,
          first_name: 'Jami',
          last_name: 'Carney',
          address: {
            country: 'England',
            city: 'London'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 21,
          first_name: 'Larsen',
          last_name: 'Shaw',
          address: {
            country: 'Canada',
            city: 'Toronto'
          },
          isDanger: false
        },
        {
          isActive: false,
          age: 89,
          first_name: 'Geneva',
          last_name: 'Wilson',
          address: {
            country: 'Australia',
            city: 'Sydney'
          },
          isDanger: false
        },
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
table{
  width:100%;
  margin-bottom: 12px;
  th{
    background-color: #dee2e6;
  }
  td,th{
    border-bottom: 1px solid #dee2e6;
    padding: 5px
  }
  .danger{
    background-color: #8CD2BC;
  }
}
</style>
