<template>
    <form @submit.prevent="setuserdata">
    <section>
        Name : <input type="text" placeholder="Enter Name" v-model="username"/>
        Age : <input type="text" placeholder="Enter Age" v-model="userage"/>
        <button> Set User Data</button>
    </section>
    </form>
</template>

<script>
export default {
    name : 'userData',
    emits : ['set-userdata'],
    data() {
        return {
            username : '',
            userage : ''
        }
    },
    methods : {
        setuserdata(){
            this.$emit('set-userdata', this.username, this.userage);
        }
    },
}
</script>