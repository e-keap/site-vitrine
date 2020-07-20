<template>
<div style="position: relative;">
  <div class="container-fluid screens-container">
    <div class="row mt-7 ">
      <div class="col-lg-1" style="height:700px" />
      <div class="col-lg-4 card-caption" :style="{'background-image': activeTabUrl, 'height': '700px'}" style="background-size: 140%;background-position: center;">
      </div>
      <div class="col-lg-6" style="height:700px;justify-content: center; align-items:center; display:flex">
        <tabs fill class="flex-column" @update-active-tab="updateActiveTab" style="width:100%">
          <card shadow>
            <tab-pane :title="item.id" v-for="(item,i) in tabs" :key="i">
              <div class="card-header"><h3 class="mb-0">{{ item.name }}</h3></div>
              <span slot="title" @click="setActiveBrand('first')">
                {{ item.name }}
              </span>
              <p class="description">{{ item.description }}</p>
              <div class="card-footer">
                <div class="d-flex justify-content-end"><small class="subtitle">{{ item.name }}</small></div>
              </div>
            </tab-pane>
          </card>
        </tabs>
      </div>
      <div class="col-lg-1" style="height:700px" />
    </div>
  </div>
  <div class="screens-row-background bg-gradient-success"></div>
</div>

</template>
<script>
  export default {
    components: {},
    data() {
      return {
        activeTab: 'Profile',
        tabs: [
          {
            id: 'Home',
            name: 'Accueil',
            description: 'L\'application mobile E.keap permet une gestion et un suivi au quotidien des tickets de caisses enregistrés. Le tout est accompagné de statistiques dès la page d\'accueil de l\'application'
          },
          {
            id: 'Scan',
            name: 'Scan',
            description: 'L\'enregistrement du ticket de caisse se fait via un écran dédié, soit par QRcode, par NFC ou par saisie manuelle dans le cas ou aucunes des deux solutions précédentes n\'est possible. Le scan est fait instantanément en pointant le module de ticket à la caisse, le ticket de carte bancaire ainsi que le ticket de caisse sont transmis à l\'application, vous êtes désormais les seuls à y avoir accès.'
          },
          {
            id: 'Ticket',
            name: 'Ticket',
            description: 'Pour des questions de garantie, vous pouvez à tout moment accéder ...'
          },
          {
            id: 'Map',
            name: 'Map',
            description: 'Lorem ipsum idem color Map'
          },
          {
            id: 'Stats',
            name: 'Statistiques',
            description: 'Lorem ipsum idem color Map'
          },
          {
            id: 'Filtre',
            name: 'Recherche',
            description: 'Lorem ipsum idem color Map'
          },
          {
            id: 'Cartes1',
            name: 'Carte Fidélité',
            description: 'Lorem ipsum idem color Map'
          }
        ]
      };
    },
    methods: {
      setActiveBrand(activeTabName) {
        // eslint-disable-next-line no-console
        console.log(activeTabName);
      },
      updateActiveTab(newTab){
        this.activeTab = newTab
      }
    },
    computed: {
      activeTabUrl() {
        return "url('img/screens/" + this.activeTab + ".png')";
      }
    },
    mounted() {
    }
  };
</script>
<style></style>