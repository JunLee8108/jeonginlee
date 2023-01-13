<template>
    <div>
        <v-divider></v-divider>
        <v-footer height="100px" padless color="white">
            <v-spacer></v-spacer>
            <v-card flat tile class="white lighten-1 text-center">
                <v-card-text class="footerText">
                    Copyright 2018. Jeong In Lee All Rights Reserved.
                </v-card-text>
                
                <br><br>
                <v-btn class="name" @click="moveAbout()" text height="40px" color="#808080">
                    <strong>About Me</strong>
                </v-btn>

                <v-btn class="name" @click="moveContact()" text height="40px" color="#808080">
                    <strong>Contact Us</strong>
                </v-btn>

                <v-card-text>
                    <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon @click="iconMove(icon)">
                        <v-icon size="24px">
                            {{ icon }}
                        </v-icon>
                    </v-btn>
                </v-card-text>

                <v-divider></v-divider>

                <v-card-text class="footerFont">
                    {{ new Date().getFullYear() }} — <strong>Jeong In Lee, Jun Lee</strong>
                </v-card-text>

            </v-card>
            <v-spacer></v-spacer>
        </v-footer>
    </div>
</template>

<script>
export default {
    name: "FooterVue",

    data: () => ({
        icons: [
            'mdi-facebook',
            // 'mdi-twitter',
            'mdi-linkedin',
            'mdi-instagram',
        ],
    }),

    methods: {
        iconMove(e) {
            if (e === "mdi-facebook") {
                window.open("https://www.facebook.com/Dave0514", "_blank");
            }
            else if (e === "mdi-instagram") {
                window.open("https://www.instagram.com/je0ngin2/?hl=ko", "_blank");
            }
            else if (e === "mdi-linkedin") {
                window.open("https://www.linkedin.com/in/jeong-in-lee-94520113b/", "_blank");
            }
        },
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
    }
};
</script>

<style scoped>
.footerClass {
    position: absolute;
    align-items: center;
    bottom: 0;
    margin: 0 auto;
    text-align: center;
    height: 0px;
}

.cardSecond {
    margin-top: -20px;
    margin-bottom: -20px;
}

.footerText {
    margin-top: 5px;
    margin-bottom: -5px;
}

.footerFont {
    font-size: 15px;
    font-family: 'Times New Roman', Times, serif;
}

.name {
    margin-bottom: -10px
}
</style>
