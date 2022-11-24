<template>
    <v-row>
        <v-col>
            <v-text-field
                v-model="valorActual"
            >
            </v-text-field>
            <v-btn @click="mostraElValor()">mostra</v-btn>
        </v-col>
        <v-col>
            <div>{{resultat}}</div>
        </v-col>
    </v-row>
</template>

<script>
export default{
    data(){
        return {
            valorActual:"",
            resultat:""
        }
    },
    methods:{
        mostraElValor(){
            this.resultat = this.valorActual
        }
    }
}
</script>