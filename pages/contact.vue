<template>
  <v-layout  justify-center align-center >
     
     
      <v-main class="contact" >
          <img src="../assets/astronaut.svg" alt="Svg of an astronaut" class="astronaut">
          <img class="moon" src="../assets/moon.svg" alt="SVG of the moon">
           <Nav />
           <Heading :pageTitle="pageTitle" />
      <v-container
        class="fill-height"
        fluid
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col
            cols="12"
            sm="8"
            md="4"
          >
            <v-card class="elevation-0">
              <v-toolbar
                color="white"
                dark
                flat
              >
                <v-toolbar-title class="primary-color">Contact form</v-toolbar-title>
                <v-spacer></v-spacer>
                
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field
                    label="Email"
                    name="email"
                    prepend-icon="mdi-email"
                    type="text"
                    class="primary-color"
                  ></v-text-field>

                  <v-textarea
                    id="message"
                    label="Message"
                    name="message"
                    prepend-icon="mdi-comment"
                    type="text"
                    class="primary-color"
                  ></v-textarea>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn  depressed class="primary-color mb-2 mr-2" >Send</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-layout>
</template>

<script>
import Nav from '../components/Nav'
import Heading from '../components/Heading'
export default {
components:{
    Nav,
    Heading
},
data(){
    return{
        pageTitle: "Let's Make Contact"
    }
}
}
</script>

<style lang="scss">
.contact{
    .astronaut{
        position: fixed;
        top: 10vh;
        right: 20vw;
        width: 25vw;
    } 
    .moon{
        position: fixed;
        bottom: 10vh;
        left: 20vw;
         width: 20vw;
    }
    height: 100vh;
    background-color: $primary;

  .v-application .primary--text {
    color: $primary !important;
    caret-color: $primary !important;
} .theme--light.v-btn:not(.v-btn--flat):not(.v-btn--text):not(.v-btn--outlined) , .theme--dark.v-sheet,.theme--light.v-icon {
        color: $primary
        }       

    .active{
        border-color: white;
    }
    .line{
        background-color: white;
    }
    .heading,a{
  color: white;
    }
  
}
</style>