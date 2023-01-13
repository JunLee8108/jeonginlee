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
            <v-btn class="name2" @click="moveContact()" text height="70px" color="#808080">
                Contact Us
            </v-btn>
            <v-spacer></v-spacer>
        </v-app-bar>
        <v-divider></v-divider>
        <!-- <v-toolbar flat height="72">
            <v-switch
              v-model="$vuetify.theme.dark"
              inset
              label="Vuetify Theme Dark"
            ></v-switch>
          </v-toolbar> -->
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
        moveContact() {
            this.$router.push({
                path: "contact",
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

@media screen and (max-width: 600px) {
    .name {
        font-size: 13px;
        margin-right: 5px;
    }
}

.name2 {
    text-align: center;
    margin-left: -10px;
    margin-right: 15px;
}

@media screen and (max-width: 600px) {
    .name2 {
        font-size: 13px;
        margin-right: 5px;
        margin-left: -5px;
    }
}
</style>
