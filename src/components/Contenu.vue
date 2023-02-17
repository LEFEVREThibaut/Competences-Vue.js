<template>
    <div>
      <h1>Les langages auxquels je me forme</h1>
      <form>
        <div class="ajout">
          <label for="action">Action</label>
          <input v-model="formData.tache" type="text" id="action">
        </div>
  
        <button v-on:click.prevent="creationItem">Ajouter la compétence</button>
      </form>
  
      <ul>
        <li v-bind:key="index" v-for="(tache,index) in tableauTaches">
          <item :id="index" :tache="tache" :suppression="suppression"></item>
        </li>
      </ul>

    </div>
  </template>
  
  <script>
  import TodoItem from './Item.vue'
  
  export default {
    name: 'TodoContenu',
    data() {
      return {
        formData: {
          tache: ''
        },
        tableauTaches: ['HTML', 'CSS', 'Tailwind CSS', 'Javascript', 'Vue JS', 'PHP']
      }
    },
    methods : {
      creationItem: function() {
        this.tableauTaches.push(this.formData.tache)
        this.formData.tache = ''
      },
      suppression: function(e) {
        this.tableauTaches.splice(e.target.parentNode, 1)
      }
    },
      components: {
        'item': TodoItem
      }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
    h1 {
      margin-top : 70px !important;
      text-align: center;
    }
  
    ul {
      list-style-type: none;
      padding: 0;
    }

    button {
      margin: 20px 165px;
      background-color: rgb(0, 106, 255);
      color: white;
      padding: 15px;
      border-radius: 8px;
      border: none;
      font-size: 18px;
    }
    .ajout {
      display: flex;
      flex-direction: column;
      margin-left: 165px;
    }

    .ajout input {
      width: 75vw;
      padding: 5px 0;
      font-size: 20px;
      padding-left: 10px;
    }
  </style>
  