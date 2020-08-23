<template>
  <v-dialog max-width="600" v-model="showDialog">
    <v-card >
      <v-card-title>{{title}}</v-card-title>
      <v-card-text>
        <v-form>
          <v-row dense>
            <v-col cols="12" >
              <v-text-field v-model="task.title" type="text" label="Título" outlined/>
            </v-col>
            <v-col cols="12">
              <v-textarea v-model="task.description" type="text" label="Descrição" outlined/>
            </v-col>
            <v-col cols="12">
              <v-btn  color="primary" class="elevation-0" block rounded  @click="save">Salvar</v-btn>
            </v-col>
          </v-row>
        </v-form>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: {
    showDialog: {
      type: Boolean,
      required: true,
    },
    title: {
      type: String,
      default: "Nova Tarefa",
    },
    task: {
      type: Object,
      required: true,
    },
    save: {
      type: Function,
      default: () => {},
    },
  },
};
</script>
