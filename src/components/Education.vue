<template>
    <v-container>
        <v-row class="text-center">
            <v-col>
                <h1 class="section">Education</h1>
            </v-col>
        </v-row>
        <v-row class="text-center">
            <v-col cols="12" xxl="6" xl="6" lg="6" md="6" sm="6" xs="12">
                <v-row>
                    <v-col></v-col>
                    <v-col cols="6" xxl="4" xl="4" lg="4" md="6" sm="6" xs="6">
                        <v-img v-if="$vuetify.theme.name === 'light'" src="@/assets/unach_light.png"></v-img>
                        <v-img v-else src="@/assets/unach.svg"></v-img>
                    </v-col>
                    <v-col></v-col>
                </v-row>
                <v-row>
                    <v-col>
                        Universidad Autónoma de Chiapas <br>
                        2009 - 2014 <br>
                        <v-icon icon="mdi-rocket-launch"></v-icon> B.S. Physics
                    </v-col>
                </v-row>
            </v-col>
            <v-col cols="12" xxl="6" xl="6" lg="6" md="6" sm="6" xs="12">
                <v-row>
                    <v-col></v-col>
                    <v-col cols="6" xxl="4" xl="4" lg="4" md="6" sm="6" xs="6">
                        <v-img src="@/assets/upchiapas.png" color="white" rounded="circle"></v-img>
                    </v-col>
                    <v-col></v-col>
                </v-row>
                <v-row>
                    <v-col>
                        Universidad Politécnica de Chiapas <br>
                        2017 - 2020 <br>
                        <v-icon icon="mdi-desktop-classic"></v-icon> B.E. Software Engineering
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-container>
</template>
