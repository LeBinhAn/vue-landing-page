<template>
    <v-container>
        <input type="text" placeholder="Search"/>
        <label for="">{{ label.text }}</label> 
    </v-container>
</template>
<script>
export default {
    name: "SearchBox",
    data: () => ({
        label: [
            {
                text: "Search",
                href: "#"
            },
        ]
    }),
}
</script>
<style>
    
</style>