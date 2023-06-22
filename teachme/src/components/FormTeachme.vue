<template>
    <div>
        <h1>FormTechme...</h1>

        <div class="card">
                <label>Nombre: </label>
                <input type="text" v-model="teacher.name">
    
                <label> Apellido Paterno: </label>
                <input type="text" v-model="teacher.surname">
    
                <label> Apellido Materno: </label>
                <input type="text" v-model="teacher.lastname">
    
                <label> N° DNI: </label>
                <input type="text" v-model="teacher.dni">
                <label> Materias:</label>
                <input type="text" v-model="materia">
                <button v-bind:onClick="materias"> Añadir Materia</button>
                <hr>
                <button :onClick="add">Enviar form</button>
        </div>

        <div>
            <table>
                <thead>
                  <tr>
                    <th>N° DNI</th>
                    <th>Nombre</th>
                    <th>Apellido Paterno</th>
                    <th>Apellido Materno</th>
                    <th>Materias</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="item in teachers" :key="item.dni">
                    <td>{{item.dni}}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.surname}}</td>
                    <td>{{item.lastname}}</td>
                    <td v-for="mat in item.materias" :key="mat">
                        <ul>
                            <li>{{mat}}</li>
                        </ul>
                    </td>
                  </tr>
                </tbody>
              </table>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { Ref, ref } from 'vue';

interface Iteach{
    name: string,
    surname: string,
    lastname: string,
    dni: string,
    materias: Array<string>, 
}

const teacher:Ref<Iteach> = ref(
    {
        name: '',
        surname: '',
        lastname: '',
        dni: '',
        materias: [],
    });

// constantes para almacenar
const materia:Ref<string> = ref('');
const teachers:Ref<Array<Iteach>> = ref([]);

//metodos para almacenar
const materias = () => {
    teacher.value.materias.push(materia.value)
    materia.value = ''
};

const add = () => {
    teachers.value.push({
        name: teacher.value.name,
        surname: teacher.value.surname,
        lastname: teacher.value.lastname,
        dni: teacher.value.dni,
        materias: teacher.value.materias,
    })
    teacher.value.name = ""
    teacher.value.surname = ""
    teacher.value.lastname = ""
    teacher.value.dni = ""
    teacher.value.materias = []
}

</script>

<style scoped>

.card{
    border: 1rem solid #d7d7d7;
    border-radius: 4px;
}

</style>