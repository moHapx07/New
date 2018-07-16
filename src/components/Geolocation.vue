<template>
  <div>
      <h1>Let us find you.</h1>
      <p>Who is this?</p>
      <input type="radio" id="surveyor" value="Surveyor" v-model="user">
      <label for="surveyor">Surveyor</label>
      <input type="radio" id="n_user" value="New User" v-model="user">
      <label for="n_user">New User</label><br>
      <span>{{user}}</span>
      <span v-html="locate"></span>        <span id="glyphicon glyphicon-copyright-mark"></span>


      
  </div>  
</template>
<script>
export default {
    name:'geolocation',
    data(){
        return{
            user: '',
            locate:"<p>Send your location to a nearby surveyor <button @:click='Send'>Send</button></p>"
                    }
    },
    methods:{
        getLocation: () => {
            if(navigator.geolocation){
                navigator.geolocation.getCurrentPosition(showPosition);
            }else{
                x.innerHTML = "Geolocation is not supported in your browser.";
            }
            
        },
        
        showPosition: (position) => {
            x.innerHTML= "Your Latitude is: " + position.coords.latitude +
             "<br> Your longitude is: " + position.coords.longitude;
        }
        ,
        //Later build send will go to the surveyors portal
        Send: () => {
            return getLocation()
        }
            
        }

    
}
</script>
<style scoped>
 h1{
        color: purple;
    }

</style>
