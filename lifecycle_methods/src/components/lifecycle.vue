<template>
    <h1>beforeCreate and created</h1>
    <h2>beforeMount and mounted</h2>
    <h1 ref="counter"> {{ count }}</h1>
    <button @click="count=count+1">Update Count</button>
</template>

<script>
export default{
  data(){
    return{
        count:0
    }
  },
   
        beforeCreate(){
            alert("before create")
        },

        created(){
            alert("created")
        },

        beforeMount(){
            console.log("beforeMount",this.$el)
        },
        mounted(){
            console.log("  mounted",this.$el)
        },

        beforeUpdate(){
            console.log("beforeUpdate",this.$refs['counter'].textContent)
        },

        updated(){
            console.log("  updated",this.$refs['counter'].textContent)
        }
   
}
</script>