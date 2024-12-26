<script setup>
    import { ref } from 'vue'
    let teacher = ref({
        name: '',
        surname: '',
        cc: '',
        subjectsOptions: [],
        doc: false    
    });
    let teachers = ref([]);
    let subject = ref([]);

    const addSubject = () => 
    {
        if (subject.value) 
        {
            teacher.value.subjectsOptions.push(subject.value);
            subject.value = '';
        }else{
            alert('Please enter a subject');
        }
        console.log(teacher.value.subjectsOptions);
    }

    const addTeacher = () => 
    {
        if (teacher.value.name && teacher.value.surname && teacher.value.cc && teacher.value.subjectsOptions.length > 0) 
        {
            teachers.value.push(teacher.value);
            teacher.value = {
                name: '',
                surname: '',
                cc: '',
                subjectsOptions: [],
                doc: false    
            };
        } else {
            alert('Please fill out all the required fields');
        }
        console.log(teachers);
    }
</script>
<style scoped>
    body {
        font-family: Arial, sans-serif;
        margin: 20px;
    }
    form {
        max-width: 400px;
        margin: 0 auto;
        justify-items: left;
    }
    label {
        display: block;
        margin-top: 10px;
    }
    input, select {
        width: 400px;
        padding: 8px;
        margin-top: 5px;
        box-sizing: border-box;
    }
    .checkbox {
        display: flex;
        align-items: center;
    }
    .checkbox input {
        width: auto;
        margin-right: 10px;
    }
    .primaryButton {
        margin-top: 20px;
        padding: 10px;
        background-color: #007BFF;
        color: white;
        border: none;
        cursor: pointer;
        width: 400px;
    }
    .primaryButton:hover {
        background-color: #0056b3;
    }
    .secundaryButton {
        margin-top: 20px;
        padding: 10px;
        background-color: #00FF7B;
        color: white;
        border: none;
        cursor: pointer;
    }
    .secundaryButton:hover {
        background-color: #00B356;
    }
</style>
<template>
    <h1>Formulario de Registro</h1>
    <form action="#" method="POST">
        <label for="nombre">Nombre:</label>
        <input type="text" v-model="teacher.name" id="nombre" name="nombre" placeholder="Ingresa tu nombre" required>

        <label for="apellido">Apellido:</label>
        <input type="text" v-model="teacher.surname" id="apellido" name="apellido" placeholder="Ingresa tu apellido" required>

        <label for="cc">Cédula de Ciudadanía (CC):</label>
        <input type="text" v-model="teacher.cc" id="cc" name="cc" placeholder="Ingresa tu número de cédula" required>

        <label for="materias">Materias:</label>
        <input type="text" v-model="subject" id="materias" name="materias" placeholder="Ingresa las materias">
        <button type="button" @click="addSubject" class="secundaryButton">agregar</button>
        <ol>
           <li v-for="materia, index in teacher.subjectsOptions" :key="index"> {{ materia }} </li> 
        </ol>
        <div class="checkbox">
            <input type="checkbox" v-model="teacher.doc" id="documentacion" name="documentacion">
            <label for="documentacion">Documentación entregada</label>
        </div>

        <button type="button" @click="addTeacher" class="primaryButton">Enviar</button>
    </form>
</template>

