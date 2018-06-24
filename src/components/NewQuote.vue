<template>
    <div>
        <p>Quote</p>
        <textarea v-model="quote"></textarea>
        <button @click='addQuote'>Add Quote</button>
    </div>
</template>
<script>
export default{
    data:function(){
        return{
            quote:''
        };
    },
    methods:{
        addQuote(){
            this.$emit('quoteAdded',this.quote);
            this.quote="";
        }
    }
}
</script>
<style>
</style>