<template>
  <q-layout view="lHh LpR lFf">
    <q-header reveal elevated style="background: linear-gradient(145deg, rgb(74, 94, 137) 15%, rgb(30, 75, 131) 70%);">
      <q-toolbar>
        <q-btn @click="left = !left" flat round dense icon="menu" class="q-mr-sm"/>
        <!--          <q-avatar>-->
        <!--            <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">-->
        <!--          </q-avatar>-->

        <q-toolbar-title>Undefined Shoes</q-toolbar-title>
        <q-btn flat round dense icon="search" class="q-mr-xs"/>
        <q-btn flat round dense icon="fas fa-sign-out-alt" to="/"/>
      </q-toolbar>
    </q-header>
    <q-drawer class="left-navigation text-white"
              show-if-above v-model="left"
              style="background-image: url(https://demos.creative-tim.com/vue-material-dashboard/img/sidebar-2.32103624.jpg) !important;"
              side="left"
              elevated>
      <div style="height: calc(100% - 117px);padding:10px">
        <q-toolbar>
          <q-avatar>
            <img src="https://i.pinimg.com/564x/19/4d/64/194d64c0df7b4753c5e190edf5fd4be6.jpg">
          </q-avatar>

          <q-toolbar-title>Phan Hoài Nam</q-toolbar-title>
        </q-toolbar>
        <hr/>
        <q-scroll-area style="height:100%;">
          <q-list padding>
            <q-item active-class="tab-active" to="/dashboard" exact class="q-ma-sm navigation-item" clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="dashboard"/>
              </q-item-section>

              <q-item-section>
                Dashboard
              </q-item-section>
            </q-item>

            <q-item active-class="tab-active" to="/customer_management" class="q-ma-sm navigation-item" clickable
                    v-ripple>
              <q-item-section avatar>
                <q-icon name="redeem"/>
              </q-item-section>

              <q-item-section>
                Products
              </q-item-section>
            </q-item>

            <q-item active-class="tab-active" to="/quotes" class="q-ma-sm navigation-item" clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="reorder"/>
              </q-item-section>

              <q-item-section>
                Categories
              </q-item-section>
            </q-item>

            <q-item active-class="tab-active" to="/employee_salary_list" class="q-ma-sm navigation-item" clickable
                    v-ripple>
              <q-item-section avatar>
                <q-icon name="shopping_cart"/>
              </q-item-section>

              <q-item-section>
                Orders
              </q-item-section>
            </q-item>

          </q-list>
        </q-scroll-area>
      </div>
    </q-drawer>

    <q-page-container style="background-color:#f1f2f6">
      <router-view/>
    </q-page-container>


  </q-layout>
</template>

<script>
    export default {
        data() {
            return {
                left: false
            }
        }
    }
</script>

<style>
  .q-drawer {
    /*background-image: url(https://demos.creative-tim.com/vue-material-dashboard/img/sidebar-2.32103624.jpg) !important;*/
    background-image: url('/statics/images/lake.jpg') !important;
    background-size: cover !important;
  }

  .q-drawer__content {
    background-color: rgba(1, 1, 1, 0.75);
  }

  .navigation-item {
    border-radius: 5px;
  }

  .tab-active {
    background-color: green;
  }
</style>
