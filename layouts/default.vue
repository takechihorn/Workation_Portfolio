<template>
  <div>
    <Header />

    <Footer />
  </div>
</template>
<script>
import { AmplifyEventBus } from "aws-amplify-vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Header,
    Footer
  },
  created() {
    AmplifyEventBus.$on("authState", info => {
      if (info === "signedIn") {
        this.$router.push("/");
      } else if (info === "signedOut") {
        this.$router.push("/signin");
      }
    });
  }
};
</script>
<style lang="scss" scoped>
</style>
