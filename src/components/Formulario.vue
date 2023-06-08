<template>
    <div>
        <form>
            <label for="">Ingrese Nombre</label>
            <input type="text" v-model="nombre"><br><br>
            <label for="">Ingrese Apellido</label>
            <input type="text" v-model="apellido"><br><br>
            <label for="">Ingrese Correo</label>
            <input type="text" v-model="correo"><br><br>
            <label for="">Ingrese Edad</label>
            <input type="text" v-model="edad"><br><br>
            <button @click.prevent="registro">Enter</button>
        </form>
        <div>
            <div v-if="edad >= 0 && edad < 14">
                Usted se encuentra en la etapa de niñez
            </div>
            <div v-if="edad >= 14 && edad < 18">
                Usted se encuentra en la etapa de Adolescencia
            </div>
            <div v-if="edad >= 18 && edad < 36">
                Usted se encuentra en la etapa de Adulto Joven
            </div>
            <div v-if="edad >= 35 && edad < 65">
                Usted se encuentra en la etapa de Adulto
            </div>
            <div v-if="edad > 64">
                Usted se encuentra en la etapa de Tercera Edad
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'component-name',
    // props: {},
    data: function () {
        return {
            nombre: "",
            apellido: "",
            correo: "",
            edad: ""
        }
    },
    // computed: {},
    methods: {
        registro() {
            //alert("Registrado")
            alert(`Saludos ${this.nombre} ${this.apellido} tu correo es ${this.correo}`)
            this.nombre = ""
            this.apellido = ""
            this.correo = ""
            this.edad = ""
        }
    }
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped></style>