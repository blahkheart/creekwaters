<template>
    <v-img cover max-height="500" src="@/assets/img/header-img.jpg" gradient="to bottom, rgba(100,115,201,.33), rgba(25,32,72,.7)">
        <v-container>
            <v-row>
                <v-col>
                    <div style="height:400px" class="header d-flex text-center flex-column justify-center align-center">
                        <h1 class="display-2 mb-2 white--text text-uppercase text-no-wrap"  v-for="heading in primaryHeading" :key="heading.text">
                            {{heading.text}}
                        </h1>
                   
                        <v-btn large rounded class="mt-5">
                            free social media audit for your business
                        </v-btn>
                    </div>
                </v-col>
            </v-row>
        </v-container>
    </v-img>
</template>

<script>
export default {
    
    data: ()=> ({
        primaryHeading: [
            {text:'Get more leads',mb:false}, 
            {text:'more customers', mb:false}, 
            {text:'more revenue', mb: true}
        ],
    })
}
</script>