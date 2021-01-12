<template>
    <div id="app">
        <active-user 
        :username="user.name" 
        :userage="user.age"
        ></active-user>
        <user-data @set-userdata="addUserData"></user-data>
    </div>
</template>

<script>
export default {
    data(){
        return{
            user : {
                name : 'Ravi',
                age : 25
            }
        };
    },
    methods : {
        addUserData(name, age){
            this.user = {
                name : name,
                age : +age
            };
        }
    }
}
</script>

<style>
html{
    font-family: sans-serif;
}
section {
    margin : 2rem auto;
    max-width: 400rem;
    border-radius: 12px;
    border : 1px solid #ccc;
    padding : 2rem;
}
</style>