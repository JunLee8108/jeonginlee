<template>
    <div>
        <NavigationVue />

        <v-card width="100%" height="700px"  color="#779ECB">
            <!-- <v-card color="#779ECB" width="30%" flat>
                <v-img src="./images/image2.jpg" height="700px"></v-img>
            </v-card>

            <v-card color="#779ECB" width="40%" flat>
                <div class="imageText">
                    Medical Tourism Specialist
                </div>
                <div class="name">
                    Jeong In Lee.
                </div>
                <center>
                    <v-btn elevation="3" height="45px">Learn More</v-btn>
                </center>
            </v-card>

            <v-card color="#779ECB" width="30%" flat>
                <v-img src="./images/image2.jpg" height="700px"></v-img>
            </v-card> -->

            <div class="wrapper">
                <div class="content">
                    <div class="imageText">
                        Medical Tourism Specialist
                        <div class="name">
                            Jeong In Lee.
                        </div>
                        <center>
                            <v-btn class="learnMoreButton" elevation="3" height="45px">Learn More</v-btn>
                        </center>
                    </div>
                </div>
              </div>

            


        </v-card>

        
        <center>
            <FooterVue />
        </center>
    </div>
</template>

<script>
import FooterVue from './Footer.vue';
import NavigationVue from './Navigation.vue';

export default {
    name: "LandingPage",

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
    font-family: 'Times New Roman', Times, serif;
    font-size: 43px;
    font-weight: bold;
    font-style: italic;
    margin-bottom: 15px;
    color: white;
}

.learnMoreButton {
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-weight: bold;
}

.imageText {
    text-align: center;
    font-family: 'Times New Roman', Times, serif;
    font-size: 38px;
    font-weight: bold;
    color: white;
}

.wrapper {
    display: grid;
    place-items: center;
    min-height: 75vh;
  }
  
  .content {
    font-family: system-ui, serif;
    font-size: 1.5rem;
    padding: 2rem;
    border-radius: 1rem;
  }
</style>
