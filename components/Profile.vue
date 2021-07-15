<template>
<div >
    <div class="profile-container" >
        <v-card
        class="mx-auto"
        max-width="450"
        tile
        elevation="5"
        >
        <v-img
        height="250px"
        :src="img"
        >
        <v-row
            align="end"
            class="fill-height"
        >
            <v-col
            align-self="start"
            class="pa-0"
            cols="5"
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
              
            <v-col 
            cols="6"
            align-self="start"
            class="profile-contact"
            >
                <div style="margin-bottom:1em">
                    <v-icon>mdi-facebook</v-icon>
                    <a>Example Facebook</a>
                </div>
                <div >
                    <v-icon>mdi-linkedin</v-icon>
                    <a>Example linkedin</a>
                </div>
            </v-col>

            <v-col>
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
        img: String
    }
}

</script>

<style scoped>
    .profile-container{
        padding: 1em;
    }
    a{
        color:rgba(255, 255, 255, 0.7);
    }
    .profile-contact{
        display: block;
        align-content: center;
        font-size: 1em;
        margin-top:3em;
    }
</style>>
    
