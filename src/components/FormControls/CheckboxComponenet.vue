<template>
    <h2 class="text-center">checkbox</h2>
    <div class="d-flex">
        <v-checkbox color="green" label="success" focused indeterminate></v-checkbox>
    <v-checkbox color="red" label="red" disabled ></v-checkbox>
    <v-checkbox color="orange" label="orange" error error-messages="error"></v-checkbox>
    <v-checkbox color="red" label="red" false-icon="mdi-close" false-value="close"></v-checkbox>
    <v-checkbox disabled :model-value="true" label="on-disabled"></v-checkbox>
    </div>
    
    <div class="text-center">{{ selected }}</div>
    <div class="d-flex">
        
        <v-checkbox label="snehal" v-model="selected" value="snehal"></v-checkbox>
        <v-checkbox label="divya" v-model="selected" value="divya"></v-checkbox>
        <v-checkbox label="shubham" v-model="selected" value="shubham"></v-checkbox>
        <v-checkbox label="sneha" v-model="selected" value="sneha"></v-checkbox>
        
    </div>
</template>

<script>
export default {
    data(){
        return{
            selected:["snehal"]
        }
    }
    
}
</script>