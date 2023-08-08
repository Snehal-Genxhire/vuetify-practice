<template>
    <h2 class="text-center">File Inputs</h2>
    <v-container>
        <v-row>
            <v-col cols="3">
                <v-file-input label="File Input"></v-file-input>
            </v-col>
            <v-col cols="3">
                <v-file-input label="Accept only Image file" accept="image/*" chips variant="solo-filled"></v-file-input>
            </v-col>
            <v-col cols="3">
                <v-file-input label="File Input" counter show-size multiple :rules="rules"></v-file-input>
            </v-col>
            <v-col cols="3">
                <v-file-input label="File Input" counter prepend-icon="mdi-camera"></v-file-input>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data(){
        return{
            rules:[
                value =>{
                    return !value || !value.length || value[0].size < 10000 ||'size should be less than 10kb'
                }
            ]
        }
    }
}
</script>