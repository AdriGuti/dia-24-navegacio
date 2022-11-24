<template>
    <v-row>
        <v-col>
            <v-text-field 
                v-model="elNumero">
            </v-text-field>
        </v-col>
        <v-col>
            <div v-text="parseInt(elNumero)*10"></div>
        </v-col>
    </v-row>
</template>
<script>
export default{
    data(){
        return {
            elNumero:""
        }
    }
}
</script>