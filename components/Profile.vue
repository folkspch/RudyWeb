<template>
<div >
    <div class="profile-container" >
        <v-card
        class="mx-auto"
        max-width="434"
        tile
        elevation="5"
    >
        <v-img
        height="100%"
        src="https://cdn.vuetifyjs.com/images/cards/server-room.jpg"
        >
        <v-row
            align="end"
            class="fill-height"
        >
            <v-col
            align-self="start"
            class="pa-0"
            cols="12"
            >
            <v-avatar
                class="profile"
                color="white"
                size="164"
                tile
            >
                <v-img src="https://cdn.icon-icons.com/icons2/1674/PNG/512/person_110935.png"></v-img>
            </v-avatar>
            </v-col>
            <v-col class="py-0">
            <v-list-item
                color="rgba(0, 0, 0, .4)"
                dark
            >
                <v-list-item-content>
                <v-list-item-title class="text-h6">
                    {{name}}
                </v-list-item-title>
                <v-list-item-subtitle>{{position}}</v-list-item-subtitle>
                </v-list-item-content>
            </v-list-item>
            </v-col>
        </v-row>
        </v-img>
    </v-card>
    </div>
</div>
</template>

<script>
export default {

    props:{
        name: String,
        position: String,
    }
}

</script>

<style scoped>
    .profile-container{
        padding: 2em;
    }
</style>>
    
