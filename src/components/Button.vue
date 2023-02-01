<template>

    <!-- click.shift yaptığım zaman shift tuşuna bastığım zaman çalışacağını söylemiş oluyorum. -->
  <div @click.shift="clean">
    <h3>Temizle</h3>
  </div>
</template>

<script>
export default {
    data(){
        return{

        }
    },
    methods:{
        clean(){
            //emit event göndermek için kullanılır.
            this.$emit('clean')
        }
    }

}
</script>

<style>

</style>