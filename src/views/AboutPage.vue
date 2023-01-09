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
    name: "AboutPage",

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
}

.name2 {
    text-align: center;
    margin-left: -10px;
    margin-right: 15px;
}

.imageText {
    text-align: center;
    font-family: 'Times New Roman', Times, serif;
    font-size: 40px;
    font-weight: bold;
}
</style>
