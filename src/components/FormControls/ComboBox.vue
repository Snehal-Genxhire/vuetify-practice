<template>
    <h2 class="text-center">ComboBox</h2>
    <v-container fluid>
        <v-row>
            <v-col cols="3"><v-combobox label="default combobox" multiple :items="items"></v-combobox></v-col>
            <v-col cols="3"><v-combobox label="i use chips" multiple chips :items="items"></v-combobox></v-col>
            <v-col cols="3"><v-combobox label="default combobox" multiple :items="items"></v-combobox></v-col>
            <v-col cols="3"><v-combobox label="readonly" :items="items" chips v-model="selected" readonly></v-combobox></v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data(){
        return{
            selected:["India", "USA", "Japan"],
            items: ["India", "USA", "Japan", "England", "Rassia"],
        }
    }
}
</script>