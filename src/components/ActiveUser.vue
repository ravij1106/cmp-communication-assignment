<template>
    <section>
        <h2>{{username}}</h2>
        <h3>{{userage}} Years</h3>
    </section>
</template>

<script>
export default {
    name : 'activeUser',
    props : ['username','userage']
}
</script>