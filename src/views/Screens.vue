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
              <p class="description" style="font-size: 1.1rem;padding: 30px;text-align: justify;">{{ item.description }}</p>
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
            description: 'Pour des questions de garantie, vous pouvez à tout moment accéder à vos tickets de caisse, les visualiser et les partager avec les personnes de votre choix'
          },
          {
            id: 'Map',
            name: 'Map',
            description: 'Une carte intéractive vous permet de trouver tous nos partenaires. Vous obtiendrez l\'adresse postale ainsi que le numéro de téléphone pour contacter notre partenaire.'
          },
          {
            id: 'Stats',
            name: 'Statistiques',
            description: 'En supplément des statistiques disponibles sur votre page d\'accueil, vous pouvez retrouver des statistiques de dépense par période, annuel, mensuel et hebdomadaire. Ces statistiques vous permettent de faire la corrélation entre votre compte en banque et vos tickets de caisse, le papier c\'est fini !'
          },
          {
            id: 'Filtre',
            name: 'Recherche',
            description: 'Une recherche de vos tickets est bien évidemment disponibles avec des filtres avancés. Ces filtres vous permettent notamment de retrouver des tickets que vous avez indiqué comme important, pour vos garanties d\'achat par exemple. De plus les classiques filtres par montant, par période et par type de paiement sont bien évidemment présents. Deux modes d\'affichages se proposent à vous, par catégorie de dépense ou par vendeur afin de vous y retrouver plus rapidement.'
          },
          {
            id: 'Cartes1',
            name: 'Carte Fidélité',
            description: 'Ce n\'est pas tout, il est possible de lié vos cartes de fidélités à votre compte, tout est centralisé au même endroit, plus besoin de 5 applications différentes pour s\'y retrouver.'
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
<style>

</style>