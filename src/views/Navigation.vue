<template>
    <div>
        <v-app-bar app elevation="0" color="white" height="70px">
            <v-spacer></v-spacer>
            <v-btn class="name" @click="moveHome()" text height="70px" color="#808080">
                Home
            </v-btn>
            <v-btn class="name" @click="moveAbout()" text height="70px" color="#808080">
                About Me
            </v-btn>
            <v-btn class="name2" text height="70px" color="#808080">
                Contact Us
            </v-btn>
            <v-spacer></v-spacer>
        </v-app-bar>
        <v-divider></v-divider>
    </div>
</template>

<script>
export default {
    name: "NavigationVue",

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
</style>
