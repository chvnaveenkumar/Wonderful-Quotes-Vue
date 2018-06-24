<template>
    <div class="row">
               <div v-for='quote in quotes' :key='quote'>
                   <div class="panel panel-default">
                     <div class="panel-body"> 
                        {{ quote }}
                      </div>
                   </div>
              </div>
    </div>    
</template>
<script>

export default {
    props:['quotes']
}
</script>
<style>
    p{
        border-block-end: 1px;
    }
</style>
