<template>
    <div>
        <div class = 'specDesc'>
            <h3><b>{{species.name}}</b></h3>
            <b>Classification:</b> {{species.classification}}<br/>
            <b>Designation:</b> {{species.designation}}<br/>
            <b>Average height:</b> {{species.average_height}}<br/>
            <b>Skin colors:</b> {{species.skin_colors}}<br/>
            <b>Hair colors:</b> {{species.hair_colors}}<br/>
            <b>Eye colors:</b> {{species.eye_colors}}<br/>
            <b>Average lifespan:</b> {{species.average_lifespan}}<br/>
            <b>Language:</b> {{species.language}}<br/>
        </div>
        <router-link class = "back" to="/">Back</router-link>
    </div>    
</template>

<script>
import axios from 'axios';
import { mapState, mapGetters } from 'vuex';

export default {
    computed: {
        ...mapState(['species']),
        ...mapGetters([
            'getSpeciesByID'
        ]),

        species() {
            return this.getSpeciesByID(this.$route.params.id)
        }
    },   
}
</script>

<style lang="scss">
h3 {
    color: white
}
.specDesc {
    margin-bottom: 15px;
}
.back {  
  padding: 10px 15px;
  border: 1px solid whitesmoke;
  border-radius: 5px;
  color:white;
  background-color: grey;
  font-size: 20px;  
  
  &:hover {
    color: grey;
    background-color: white;
    font-size: 20px;
  }
}
</style>

