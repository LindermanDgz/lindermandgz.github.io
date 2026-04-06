<template>
    <v-container>
        <v-row>
            <v-col></v-col>
            <v-col cols="12" xxl="6" xl="6" lg="8" md="8" sm="8" xs="12">
                <v-row>
                    <ContactInfo />
                </v-row>
                <v-row>
                    <Stack />
                </v-row>
                <v-row>
                    <Education />
                </v-row>
                <v-row>
                    <Experience />
                </v-row>
            </v-col>
            <v-col></v-col>
        </v-row>
    </v-container>
</template>

<script setup>
  import ContactInfo from '@/components/ContactInfo.vue'
  import Stack from '@/components/Stack.vue'
  import Education from '@/components/Education.vue'
  import Experience from '@/components/Experience.vue'
</script>
