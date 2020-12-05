<template>
        
            <!-- Card-->

            <div class="card shadow-sm border-0 rounded" style="height: 400px;">
                <div class="card-body"><img :src="member.image" alt="Imagen del equipo"  class="w-100 card-img-top h-50">
                    <div class="p-4">
                        <h5 class="mb-0">{{member.nombre}}</h5>
                        <p class="small text-muted"> {{member.rol}}</p>
                        <p class="text-justify">{{member.descripcion}}</p>
                    </div>
                </div>
            </div>


</template>

<script>
    export default {
        name: "TeamCard",
        props: [ 'member'],
    }
</script>


<style scoped>

</style>
