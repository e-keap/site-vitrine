<template>
<div style="position: relative;">
  <div class="container-fluid screens-container">
    <div class="row mt-7 ">
      <div class="col-lg-4 card-caption" :style="{'background-image': activeTabUrl}">
      </div>
      <div class="col-lg-8">
        <tabs fill class="flex-column flex-md-row" @update-active-tab="updateActiveTab">
          <card shadow>
            <tab-pane title="bb-yoda">
              <div class="card-header"><h3 class="mb-0">Title - Anazenaze azejaze aeazel</h3></div>
              <span slot="title" @click="setActiveBrand('first')">
              <i class="ni ni-cloud-upload-96"></i>
                Home
              </span>
              <p class="description">Raw denim you probably haven't heard of them jean shorts
                Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache
                cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro
                keffiyeh dreamcatcher synth.</p>
              <div class="card-footer">
                <div class="d-flex justify-content-end"><small class="subtitle">Project- nom de la vue</small></div>
              </div>
            </tab-pane>

            <tab-pane title="yoda">
            <span slot="title" @click="setActiveBrand('second')">
              <i class="ni ni-bell-55 mr-2"></i>
                Profile
            </span>
              <div class="card-header"><h3 class="mb-0">Title -2</h3></div>

              <p class="description">Cosby sweater eu banh mi, qui irure terry richardson ex
                squid. Aliquip placeat salvia cillum iphone. Seitan aliquip quis cardigan
                american apparel, butcher voluptate nisi qui.</p>
              <div class="card-footer">
                <div class="d-flex justify-content-end"><small class="subtitle">Project- nom de la vue</small></div>
              </div>
            </tab-pane>

            <tab-pane title="bb-yoda">
             <span slot="title" @click="setActiveBrand('third')">
               <i class="ni ni-calendar-grid-58"></i>
                Messages
              </span>
              <div class="card-header"><h3 class="mb-0">Title -3 </h3></div>
              <p class="description">Raw denim you probably haven't heard of them jean shorts
                Austin. Nesciunt tofu stumptown aliqua, retro synth master cleanse. Mustache
                cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro
                keffiyeh dreamcatcher synth.</p>
              <div class="card-footer">
                <div class="d-flex justify-content-end"><small class="subtitle">Project- nom de la vue</small></div>
              </div>
            </tab-pane>
          </card>
        </tabs>
      </div>
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
        activeTab: 'Profile'
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