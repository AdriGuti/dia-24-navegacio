<template>
    <div>
        <v-img
            width="100vw"
            height="100vh" 
            src="https://images.pexels.com/photos/8388229/pexels-photo-8388229.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">
            <v-container full-height>
                <v-row style="heigth:100%" align="center" justify="center">
                    <v-col>
                        <h1 style="color:white">COMPRA'M!</h1>
                        <v-text-field
                        dark
                        label="El teu email" 
                        ></v-text-field>
                        <v-btn>Compra</v-btn>
                    </v-col>
                </v-row>
            </v-container>
        </v-img>
    </div>
</template>
<script>
    export default{
        layout:"marketing"
    }
</script>