<template>
<div class="divContainer">
  <v-card class="divContainer" v-for='(item, index) in tasks' :key='index' >
      <v-card-title>{{item.title}}</v-card-title>
      <v-card-text>{{item.description}}</v-card-text>
    </v-card>
</div>
</template>

<script>
export default {
  props:{
    tasks:{
      type:Array,
      requerid:true,
    }
  }
}
</script>

 
</style>