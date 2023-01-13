<template>
    <div>
        <NavigationVue />

        <br><br>
        <center>
            <FooterVue />
        </center>
    </div>
</template>

<script>
import FooterVue from './Footer.vue';
import NavigationVue from './Navigation.vue';

export default {
    name: "ContactPage",

    components: {
        FooterVue,
        NavigationVue,
    },

    data: () => ({

    }),

    methods: {
        moveAbout() {
            this.$router.push({
                path: "about",
            });
        },
        moveHome() {
            this.$router.push({
                path: "/",
            });
        },

    },
};
</script>

<style scoped>
.name {
    text-align: center;
    margin-right: 15px;
    color: white;
}

.name2 {
    text-align: center;
    margin-left: -10px;
    margin-right: 15px;
}

.imageText {
    text-align: center;
    font-family: 'Times New Roman', Times, serif;
    font-size: 30px;
    font-weight: bold;
    color: white;
}

.wrapper {
    display: grid;
    place-items: center;
    min-height: 50vh;
  }
  
  .content {
    font-family: system-ui, serif;
    font-size: 1.5rem;
    padding: 2rem;
    border-radius: 1rem;
  }

  .divBorder {
    border: 3px solid; 
    width: 405px; 
    height: 420px; 
    margin: 10px auto; 
    border-radius: 5px; 
    padding: 10px; 
    color: white;
  }
</style>
