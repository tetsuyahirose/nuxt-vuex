<template>
  <section class="container">
    <div>
      <!-- <p>{{ $store.state.message }}</p> -->
      <p>{{ $store.state.hello.message }}</p>
      <!-- <button
        v-on:click="$store.commit('updateMessage', 'Commit with payload')"
      >
        Updated
      </button> -->
      <button
        v-on:click="
          $store.dispatch('hello/updateMessageAction', 'Dispatch with payload')
        "
      >
        Dispatch
      </button>
    </div>
  </section>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
  components: {
    Logo,
    VuetifyLogo,
  },
};
</script>
