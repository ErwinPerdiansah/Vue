<template lang="">
    <div>
        <h1>ini my repo</h1>
        <table>  
            <tr>
    </div>
</template>
<script>
export default {
    methods: {
        getReposiories(){
            this.axios.get('/api/repsitories')
            .then((response) => {
                console.log(response);
            })
        }
    },
}
mounted() {
    this.getRepositories()
}
</script>
<style lang="">
    
</style>
</div>
</template>
<script>
export default {
    data() {
        return {
            repositories []
        }
    }
}
methods: {
    getrepositories() {
        this.axios.get('/api/repositories')
        .then((response) => {
            console.log(response.data.repositories);
            this.repositories = response.data.repositories
        })
    }
}