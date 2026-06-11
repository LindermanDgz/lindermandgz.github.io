<template>
    <v-container>
        <v-row class="text-center">
            <v-col>
                Job Experience
            </v-col>
        </v-row>
        <v-row>
            <v-col class="d-none d-md-block">
                <v-timeline truncate-line="start">
                    <v-timeline-item v-for="(role, i) in roles" :key="i" dot-color="blue-lighten-3" fill-dot
                        icon="mdi-briefcase" :icon-color="$vuetify.theme.name === 'light' ? 'white' : 'black'"
                        width="100%">
                        <template v-slot:opposite>
                            <p v-text="`${role.date.start} - ${role.date.end}`"></p>
                        </template>
                        <v-card class="text-center" variant="tonal">
                            <v-card-title v-text="role.name">
                            </v-card-title>
                            <v-card-subtitle>
                                <v-icon icon="mdi-domain"></v-icon> <v-text v-text="role.company"></v-text>
                                <v-spacer></v-spacer>
                                <v-icon icon="mdi-map-marker"></v-icon> <v-text v-text="role.work_model"></v-text>
                            </v-card-subtitle>
                            <v-card-text v-text="role.description"></v-card-text>
                        </v-card>
                    </v-timeline-item>
                </v-timeline>
            </v-col>
            <v-col class="d-md-none text-center">
                <v-card v-for="(role, i) in roles" :key="i" variant="tonal" class="mb-4">
                    <v-card-title v-text="role.name">
                    </v-card-title>
                    <v-card-subtitle>
                        <v-icon icon="mdi-domain"></v-icon> <v-text v-text="role.company"></v-text>
                        <v-spacer></v-spacer>
                        <v-icon icon="mdi-map-marker"></v-icon> <v-text v-text="role.work_model"></v-text>
                    </v-card-subtitle>
                    <v-card-text v-text="role.description"></v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            roles: [
                {
                    name: 'DevOps Engineer',
                    company: 'Oracle Corporation',
                    date: {
                        start: "Sep 2024",
                        end: "Mar 2026",
                    },
                    description: "OCI Oracle Linux Services",
                    work_model: "Remote",
                },
                {
                    name: 'Software Engineer',
                    company: 'Intel Corporation',
                    date: {
                        start: "Jan 2022",
                        end: "Jul 2023",
                    },
                    description: "RTL Development and CI/CD",
                    work_model: "Remote",
                },
                {
                    name: 'Graduate Technical Intern',
                    company: 'Intel Corporation',
                    date: {
                        start: "Nov 2020",
                        end: "Nov 2021",
                    },
                    description: "RTL Development and CI/CD",
                    work_model: "Remote",
                },
                {
                    name: 'Back End Python Developer',
                    company: 'Universidad Intercultural de Chiapas',
                    date: {
                        start: "Sep 2020",
                        end: "Dec 2020",
                    },
                    description: "RESTful API development with Django framework",
                    work_model: "Remote",
                },
                {
                    name: 'Fullstack Developer Angular',
                    company: 'Adiante Apps',
                    date: {
                        start: "May 2020",
                        end: "Sep 2020",
                    },
                    description: "WEB and Mobile application development using Angular",
                    work_model: "Remote",
                },
            ],
        }
    },
}
</script>
