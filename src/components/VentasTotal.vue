<template>
    <div>
        <table class="tg">
            <thead>
            <tr>
                <th class="tg-0pky">Codigo</th>
                <th class="tg-0pky">Nombre</th>
                <th class="tg-0pky">Precio</th>
            </tr>
            </thead>
            <tbody>
                <div class="lista_totales">
                    <ul>
                        <li v-for="venta in ventas" :key="venta.codigo">
                            <span>
                                <b>Codigo:</b> {{venta.id}} | 
                                <b>Nombre:</b> {{venta.nombre}} |
                                <b>Precio:</b> ${{venta.precio}}
                            </span>
                        </li>
                    </ul>
                </div>
            </tbody>
        </table>    
    </div>
</template>

<script>
export default {
    name: 'ventastotal-component',
    props: {
        juegosConStock:{
            type:Array,
        },
        ventas:{},
        sumaVentasTotal:{},
    },
    data: function(){
        return {}
    },
}
</script>

<style scoped>
    .tg {
        border-collapse:collapse;
        border-spacing:0;
        }
    .tg td {
        border-color:black;
        border-style:solid;
        border-width:1px;
        font-size:16px;
        overflow:hidden;
        padding:10px 5px;
        word-break:normal;
        }
    .tg th {
        border-color:black;
        border-style:solid;
        border-width:1px;
        font-size:16px;
        font-weight:normal;
        overflow:hidden;
        padding:10px 5px;
        word-break:normal;
        }
    .tg .tg-0pky {
        border-color:inherit;
        text-align:left;
        vertical-align:top
        }
</style>
